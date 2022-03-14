# my_daily_notes
Record what you learn every day.

### windows11 安装 Node.js

下载并安装 Node.js，下载链接为： [Node.js](https://nodejs.org/en/download/) 

windows11系统 环境变量配置  
- 在 Node.js 安装路径下 创建两个文件夹【node_global】及【node_cache】  

- 在 Node.js 安装路劲下 开启 powershell 并输入设置命令

  ```shell
  npm config set prefix "E:\Program Files\node_global"
  npm config set cache "E:\Program Files\node_cache"
  ```

- 进入环境变量对话框，

  1. 在【系统变量】下新建【NODE_PATH】，输入`E:\Program Files\nodejs\node_modules`

  2. 将【用户变量】下的【Path】将 .../AppData/Roaming/npm 修改为`E:\Program Files\node_global

Node.js 安装测试

```shell
npm install -g express
```

安装完成

```shell
(base) PS C:\Users\Mloong> node -v
v16.14.0
(base) PS C:\Users\Mloong> npm -v
8.3.1
```

### windows11 安装 Vue.js

安装 cnpm 

cnpm是淘宝的一个镜像，安装之后可以使用cnpm安装命令工具，安装速度会加快。

```shell
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

在【系统变量】下的【Path】中，添加环境变量路径 `E:\Program Files\node_global`

安装 Vue.js，并安装 Vue.js 的命令行工具，即 vue-cli 脚手架

```
cnpm install vue -g
cnpm install vue-cli -g

cnpm install webpack -g
cnpm install -g vue-router

vue -V
```

新建 vue 工程

```shell
(base) PS C:\Users\Mloong\Desktop> vue init webpack nihao

? Project name nihao
? Project description A Vue.js project
? Author Mloong <1091403476@qq.com>
? Vue build standalone
? Install vue-router? Yes
? Use ESLint to lint your code? No
? Set up unit tests No
? Setup e2e tests with Nightwatch? No
? Should we run `npm install` for you after the project has been created? (recommended) npm

   vue-cli · Generated "nihao".


# Installing project dependencies ...
# ========================
# Project initialization finished!
# ========================

To get started:

  cd nihao
  npm run dev
```







































