# vue-demos

# demo01 vue 基本指令(Directives)

v-bind v-if v-for v-on v-model v-once v-html

**Mustache 标签**

**1、概述**

Mustache 是基于 JavaScript 实现的模版引擎，该模版更加的轻量级，语法更加的简单易用。

**2、语法**

Mustache 的模板语法很简单，用于 HTML，配置文件，源代码等。它的工作方式是通过以哈希值或者对象的方式扩展模板标签。

-  {{keyName}}

`{{}}`就是 Mustache 的标示符，花括号里的 keyName 表示键名，这句的作用是直接输出与键名匹配的键值。

-  {{#keyName}} {{/keyName}}

以`#`开始、以`/`结束表示区块，它会根据当前上下文中的键值来对区块进行一次或多次渲染。

-  {{^keyName}} {{/keyName}}

该语法与`{{#keyName}} {{/keyName}}`类似，不同在于它是当 keyName 值为 null, undefined, false 时才渲染输出该区块内容。

-  {{.}}

`{{.}}`表示枚举，可以循环输出整个数组。

-  {{<partials}}

以`>`开始表示子模块，如{{> address}}；当结构比较复杂时，我们可以使用该语法将复杂的结构拆分成几个小的子模块。

-  {{{keyName}}}

`{{keyName}}`输出会将等特殊字符转译，如果想保持内容原样输出可以使用`{{{}}}。`

-  {{!comments}}

`!`表示注释，注释后不会渲染输出任何内容。

**修饰符**

修饰符 (modifier) 是以半角句号 `.` 指明的特殊后缀，用于指出一个指令应该以特殊方式绑定。例如，`.prevent` 修饰符告诉 `v-on` 指令对于触发的事件调用 `event.preventDefault()`：

```
<form v-on:submit.prevent="onSubmit">...</form>
```
