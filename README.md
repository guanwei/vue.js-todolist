# Vue+Webpack打造todo应用

根据慕课网教程 https://www.imooc.com/learn/935，以及 参考代码 https://github.com/carrieguo/vue.js-todolist 实现的一个todolist demo。

学习vue不仅仅是api,要学习整个vue生态环境，vue-router，vuex，组件开发，webpack配置。

## 如何快速启动项目

```
git clone https://github.com/guanwei/vue.js-todolist
cd vue.js-todolist
npm install
npm run dev
```

**本项目基于webpack4**

> 从4.0版本开始`CommonsChunkPlugin`被移除且被`optimization.splitChunks`和`optimization.runtimeChunk`配置项代替。

## 一步步安装依赖包

- 安装vue
```
npm i vue
```

- 安装webpack
```
npm i -D webpack@4 webpack-cli
```

- 安装相应的loader
```
npm i -D css-loader@5
npm i -D vue-loader vue-template-compiler
npm i -D stylus-loader@4
npm i -D url-loader file-loader
```

> webpack 配置中需要添加 Vue Loader 的插件 参考 https://vue-loader.vuejs.org/zh/guide/#vue-cli

- 安装`webpack-dev-server`和`cross-env`
```
npm i -D webpack-dev-server cross-env
```

> `webpack-dev-server`插件提供一个简单的本地调试服务器<br/>
> `cross-env`插件解决了跨平台设置环境变量的问题

- 安装其他依赖
```
npm i -D html-webpack-plugin@4

npm i -D babel-loader @babel/core @babel/preset-env
npm i -D babel-plugin-transform-vue-jsx babel-plugin-syntax-jsx

npm i -D postcss-loader@4 autoprefixer
```

> `babel`插件用于转译JavaScript文件

- 安装`extract-text-webpack-plugin`
```
npm i -D mini-css-extract-plugin@1
```

> `extract-text-webpack-plugin`插件被废弃，使用替代品`mini-css-extract-plugin`插件

- 安装`clean-webpack-plugin`
```
npm i -D clean-webpack-plugin
```

> `clean-webpack-plugin`插件可以在每次编译前删除之前构建生成的文件夹

## 本地运行调试
```
npm run dev
```

## 编译生成
```
npm run build
```