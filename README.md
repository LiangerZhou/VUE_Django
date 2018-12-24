# VUE_Django
vue整合Django

本程序参照https://cloud.tencent.com/developer/article/1005607，一步步搭建

其中遇到如下几点问题
使用的vue的版本为3.2.1, 使用vue create appfront创建vue项目 目录结构和vue-cli版本的稍微有所区别，参见https://cli.vuejs.org/zh/guide/creating-a-project.html#vue-create
使用的axios请求后台json数据，
    1、安装 npm install axios -S
    2、在main.js内使用
        import axios from 'axios'
        Vue.prototype.$http = axios
    3、在使用过程中，请求返回的数据，不再需要经过Json解析，因为axios请求本身返回的就是json数据

使用element-ui
    1、安装 npm i element-ui -S
    2、在main.js内使用
        import ElementUI from 'element-ui'
        import '../node_modules/element-ui/lib/theme-chalk/index.css'
        Vue.use(ElementUI)
    3、在templete内的scope要改为slot-scope，前者已经被弃用


前端vue的启动命令：npm run serve

后端 python manage.py runserver