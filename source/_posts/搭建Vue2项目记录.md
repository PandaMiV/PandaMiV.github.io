---
title: 搭建Vue2项目记录
date: 2024-06-01 12:10:18
tags:
- 博客
- hexo
- github
- 菜鸟学习
categories: 努力的前端
---
### 1、设置
      module.exports = {
        parser: 'vue-eslint-parser',
        parserOptions: {
          parser: 'babel-eslint',
          // ecmaVersion: 'latest',
          ecmaVersion: 12,
          sourceType: 'module',
          allowImportExportEverywhere: true, // 不限制eslint对import使用位置
          ecmaFeatures: {
            modules: true,
            legacyDecorators: true
          }
        },
        rules: {
          // 关闭名称校验
          "vue/multi-word-component-names": "off",
        },
      };
### 2、封装路由
### 3、封装axios请求
### 4、vue-i18n搭建多语言环境
-vue2.0要用8版本的，使用9版本的会报错
      npm install vue-i18n@8.27.0 --save
-在src目录下，新建i18n文件夹
  在新文件夹i18n中新建langs文件夹，里边放语言文本文件.js
    zh.js：存放所有的中文显示内容
      export default {
        //中文
        变量名:"中文"
      }
    en.js：存放所有的英文显示内容
      export default {
        //英文
        变量名:"英文"
      }
  与langs文件夹同级，创建index.js：用于配置i18n，并导出i18n
      import Vue from "vue"
      import VueI18n from "vue-i18n"
      //引入自定义语言配置  
      import zh from './langs/zh'
      import en from './langs/en'
      
      Vue.use(VueI18n); // 全局注册国际化包
      
      // 准备翻译的语言环境信息
      const i18n = new VueI18n({
        locale: sessionStorage.getItem('lang') || "简", //将语言标识存入localStorage或sessionStorage中，首次默认中文显示，非首次则以localStorage为准
        messages: {
          // 中文语言包
          'ZH': {
            ...zh
          },
          //英文语言包
          'ENG': {
            ...en
          }
        },
        silentTranslationWarn: true, //解决vue-i18n黄色警告"value of key 'xxx' is not a string"和"cannot translate the value of keypath 'xxx'.use the value of keypath as default",可忽略
        globalInjection: true, // 全局注入
        fallbackLocale: '简', // 指定的locale没有找到对应的资源或当前语种不存在时，默认设置当前语种为中文
      });
      
      export default i18n
  在main里导入语言包文件：main.js
      import i18n from './i18n'
    
      Vue.use(
        {
          i18n: (key, value) => i18n.t(key, value) // 在注册Element时设置i18n的处理方法,可以实现当点击切换按钮后，elementUI可以自动调用.js语言文件实现多语言切换
        }
      )
      
      new Vue({
        render: h => h(App),
        i18n
      }).$mount('#app')
  切换语言：
      changeLanguage() {
        let locale = localStorage.getItem('language') || 'zh-CN';
        let temp = locale === 'zh-CN' ? 'en-US' : 'zh-CN';
        this.$i18n.locale = temp;
        localStorage.setItem('language', temp);
      },


### 问题记录
路由守卫中this.$store获取vuex失败：
  在vue-router的路由守卫中，this并不指向vue实例，所以这个时候需要换一种方法获取。
  例如在main.js中，使用路由守卫并在路由守卫中获取vuex中数据可以这样：
    1、引入vuex实例
        import vuex from './store/index';
    2、在路由守卫中使用引入的vuex实例.state的方式获取vuex中的数据
        router.beforeEach((to, from, next) => {
          console.log(vuex.state.xxx);
        })
