1.--save:保存到dependencies(生产模式依然在用的依赖)
  --save-dev：保存到devDependencies(只在开发模式使用的依赖)
2.相关依赖:
react.js [必需]
    React是用来构建用户界面的js库，属于view层。
    它有两大特点：1，单向数据绑定；2，虚拟DOM
    安装：npm install --save react

react-dom.js [必需]
    react.js 主要用来创建元素和组件，当你想在html中渲染你的组件的时候，
    你还得需要react-dom.js。同时，react-dom.js依赖于react.js。
    安装：npm install --save react-dom

webpack [必需]
    于人而言，尤其是当开发大型项目时，每个包每个模块每个静态资源都应尽可能的条理清晰的罗列出来，
    这样方便我们开发；于机器而言，就不需要这么“条理清晰”了，此时应最大限度的压缩优化这些资源，
    如何把这些资源模块“杂糅”在一起，这就是webpack要做的。
    安装：npm install --save-dev webpack

webpack-dev-middleware [开发需要]
    它是一个用来组织包装webpack使其变成中间件的容器。（中间件的用途就是在输入和输出的过程中加工的一种手段）
    webpack本身只负责打包编译，webpack-dev-server是协助我们开发的服务器，这个服务器底层是靠express操作的。
    我们的页面如何在这个服务器上更新呢，首先是取得webpack打包好的资源，这就需要在请求到响应的过程中通过
    express的中间件取得资料， 而方法就是通过webpack-dev-middleware来实现。
    这个中间件只在开发环境中使用，切忌用在生产环境中。
    安装：npm install --save-dev webpack-dev-middleware
