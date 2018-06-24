# 用canvas实现下雨效果

## 要掌握的知识点
1. arguments.callee
2. window.onresize事件
3. js使用动画的要点
4. es6的class知识

## 开发步骤
1. 创建一个canvas区域
2. 在js中获得canvas区域
3. 给window注册resize事件，创建两个全局变量w和h，实时获取窗口的宽高
4. 创建rain类，里面包含init(),draw(),move()这三个重要方法
5. 创建raindrop类，里面包含createRain(),animation()这两个重要方法
6. raindrop依赖rain，在rain类中实现雨滴的行为，在raindrop类中包含很多雨滴

## 技术难点
### arguments.callee
[arguments.callee](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/arguments/callee)  
callee 是 arguments 对象的一个属性。它可以用于引用该函数的函数体内当前正在执行的函数。这在函数的名称是未知时很有用，例如在没有名称的函数表达式 (也称为“匿名函数”)内。

### window.onresize事件
[window.onresize](https://developer.mozilla.org/zh-CN/docs/Web/API/GlobalEventHandlers/onresize)  
onresize属性可以用来获取或设置当前窗口的resize事件的事件处理函数

### js使用动画的要点
首先要知道，屏幕刷新率，只要动画的刷新率大于等于屏幕刷新率，在人眼看来就是动画了，我的笔记本的屏幕刷新率是60Hz，每秒刷新60次，在js中，只有每秒刷新60次就行了，刷新多了显示不出来  
在这个项目中还用到了一个障眼法，每次在绘制新的动画前，都把原来的动画覆盖上一层透明度，这样最早绘制在屏幕上的动画，会越来越暗，在人眼中就变成了动画

### es6的class知识
具体参考阮一峰的这本书上的知识点[es6的class知识](http://es6.ruanyifeng.com/#docs/class#this-的指向)

