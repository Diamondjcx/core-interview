1. 写法上反复横跳 props、method、computed（用户编写复杂业务逻辑会出现反复横跳问题
2. 都要通过 this 访问
3. vue2 中很多没有使用的方法和属性依然会被打包，并且所有全局 api 都在 vue 对象上公开，CompositionAPI 对 tree-shaking 更加友好，代码也更容易压缩。
4. 组件逻辑共享问题，Vue2 采用 mixins 实现组件之间的逻辑共享：但是会有数据来源不明确，命名冲突等问题。Vue3 采用 CompositionAP1 提取公共逻辑非常方便
