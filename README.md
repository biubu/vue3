### 自定义@vue/cli 3.x 
1. 默认添加了eslint 自定义规则
1. 默认如果存在enlint报错不允许提交到git 
1. 默认 添加了vuex,vue-router
1. 默认添加了less预处理器
1. 默认相关的配置文件保存在 package.json 中

---

### 使用方法:
> 确保你安装了官方最新版的`@vue/cli`,如果没有安装，请参照[官方文档](https://cli.vuejs.org/zh/guide/installation.html)正确安装。

` vue create --preset biubu/vue3 your_project_name`

---

### 关于eslint报错 : 

这跟自定义的规则有关,官方默认生成是 2 个空格,配置文件使用的是4个空格, 官方脚手架默认的是不使用分号,配置文件强制使用分号.
用官方自带的工具修复一下即可.
`npm run lint ` 或 `yarn lint` 即可.

关于
`Line 11 exceeds the maximum line length of 120 (max-len) at src/components/HelloWorld.vue:11:1:
`的报错:
因为限定的每行长度不能超过120个字符所以会出现这个报错.解决办法:
删除`HelloWorld.vue`中 ul 和 ul 的子元素就行,正式开发的时候用不到这个组件里面的内容。
