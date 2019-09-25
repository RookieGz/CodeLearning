### this

**什么是this？**

this 实际上是在函数被调用时发生的绑定，它指向什么完全取决于函数在哪里被调用。

**this绑定方式**

* 默认绑定
* 隐示绑定
* 显示绑定
* new绑定

**绑定优先级：**

new绑定>显示绑定>隐式绑定>默认绑定

1. 函数是否在 new 中调用（new 绑定）？如果是的话 this 绑定的是新创建的对象

2. 函数是否通过 call、apply（显式绑定）或者硬绑定调用？如果是的话，this 绑定的是 指定的对象。

3. 函数是否在某个上下文对象中调用（隐式绑定）？如果是的话，this 绑定的是那个上 下文对象。

4. 如果都不是的话，使用默认绑定。如果在严格模式下，就绑定到 undefined，否则绑定到 全局对象。 

**箭头函数的this**

箭头函数执行时的上下文

**特殊情况（出自《你不知道的Javascript》）**

如果你把 null 或者 undefined 作为 this 的绑定对象传入 call、apply 或者 bind，这些值在调用时会被忽略，实际应用的是默认绑定规则

软绑定