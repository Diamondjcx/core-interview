1.  什么是 Router，以及 Router 发展的历史。
    路由的概念，是伴随 SPA 出现的。在此之前，页面的跳转是通过服务器端进行控制的；

                    传统的页面的跳转，是通过前端向后台发送请求
                    后台通过模板引擎的渲染，将一个新的 html 界面
                    比如页面跳转时：
                    	from 表单的提交；
                    	a标签的默认属性；
                    	js 调用 location.href，给其赋值；
                    	H5: history 的 go / forward / back -- // history.push / replace?


        在 SPA（即只有一个 html ）的出现后，前端可以自由控制组件的渲染，来模拟页面的跳转。

                页面是怎么发生跳转，向服务端请求的呢？-一浏览器劫持。
                在讲这部分内容前，我们先来说一下，hash 路由和 history 路由的区别
                SPA的方法，需要拦截请求；
                	hash 路由，当我的hash
                	history 的 go / forward / back 的时候，我的浏览器的地址，是发生了改变的，
        hashchange
        pushState 和 replaceState

    总结：

        后端路由是根据 url 访问相关的 controller 进行数据资源和模板引擎的拼接，返回前端；
        前端路由是通过 js根据 url 返回对应的组件加载。
        所以，前端的路由包含两个部分：
        	url 的处理
        	组件加载
