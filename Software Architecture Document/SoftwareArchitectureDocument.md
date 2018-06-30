## Software Architecture Document

| 版本 | 日期 | 描述 | 作者|
| -- | -- | -- | -- |
| 草案 | 2018.6.3 | 主要从架构问题、解决方案说明、逻辑视图、物理视图这四个方面进行描述 | lianqy |

### 架构设计

采用前后端分离开发，前端使用vue进行开发，后端使用go + mongodb进行开发。

架构图如下：

### 解决方案说明
#### 数据传递
使用Vuex（一个专为 Vue.js 应用程序开发的状态管理模式）进行状态管理。Vue采用的是单向数据流动的数据传递方式，一单遇到多个组件共享数据时便会产生诸多不便。Vuex采用集中式存储管理应用的所有组件的状态，并以相应的规则保证状态以一种可预测的方式发生变化。Vuex把组件的共享状态抽取出来，以一个全局单例模式管理，使得我们的组件无论在组件树的任何一个位置，都可以获取状态或者触发行为，减少了数据的冗余和繁复的父子组件事件触发，从而让我们的代码变得更结构化且易维护。
  
![Vuex](https://vuex.vuejs.org/vuex.png)

### 逻辑视图

![逻辑视图](https://github.com/gogogoSYSU/documents/blob/master/img/jiagouluojishitu.PNG?raw=true)

### 物理视图

![物理视图](https://github.com/gogogoSYSU/documents/blob/master/img/wuli.PNG?raw=true)
