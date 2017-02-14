## 关于vue-cli初始化项目的那些坑
> Vue.js是最近非常火爆的一个前端js框架，后面使用vue-cli建设自己的项目遇到了比较多的坑

* 开发项目的必要环境

  - node.js环境

  - npm镜像

> - 安装node.js

        使用node -v出现版本号即安装成功

> -安装vue-cli脚手架构建工具

>在命令行中运行 **npm install -g vue-cli** ,等待其安装完成


> -在自己的项目目录下，使用命令行运行命令 **vue init webpack vueProject**,此时，我们可能会遇到这种问题：

  **"Failed to download repo   vuejs-templates/webpack-simple"**
   >### 解决方案如下
   1.打开终端（cmd），输入命令：ping 192.30.253.112 发现连接超时；输入命令：ping github.com 显示超时。

  >2.打开 hosts文件，地址：C:\Windows\System32\drivers\etc  看是否是默认配置。
  >3.在本地hosts文件中加入:
  - 192.30.253.112 github.com
  - 151.101.88.249 github.global.ssl.fastly.net>

 ### 如果本地已经做了代理

 1、关闭npm的https

    npm config set strict-ssl false

2、设置npm的获取地址

    npm config set registry "http://registry.npmjs.org/"
