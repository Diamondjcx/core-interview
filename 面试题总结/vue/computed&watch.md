computed/watch，都是基于 watcher/effect

vue2 中有三种 watcher（渲染 watcher、计算属性 watcher、用户 watcher）

vue3 有三种 effect（渲染 effect、计算属性 effect、用户 effect）

## computed

特点：

    计算属性仅当用户取值时才会执行对应的方法
    有缓存的，依赖值不发生变化，对应取值计算属性不会重新执行
    计算属性可以简化模版中复杂表达式
    计算属性中不支持异步逻辑
    可以在模版中使用
    从首次生成赋值，就开始计算运行了
    内部实现：dirty：true/false 用来标识

## watch

监控值的变化，当值发生变化时调用对应的回调函数，经常用于监控某个值的变化，进行一些操作

首次不会运行，除非——immediate：true

##### 面试点 3：computed 和 watch

相同点：

1. 基于 vue 的依赖收集机制
2. 都是被依赖的变化触发，进行改变进而进行处理计算

不同点：

1. 入和出
   computed: 多入单出 —— 多个值变化，组成一个值的变化
   watch: 单入多出 —— 单个值的变化，进而影响一系列的状态变更

2. 性能
   computed: 会自动 diff 依赖，若依赖没有变化，会改从缓存中读取当前计算值
   watch: 无论监听值变化与否，都会执行回调

3. 写法上
   computed: 必须有 return 返回值
   watch: 不一定

4. 时机上
   computed: 从首次生成赋值，就开始计算运行了
   watch: 首次不会运行，除非——immediate：true
