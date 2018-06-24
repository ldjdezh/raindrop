# 用canvas实现下雨效果

## 要掌握的知识点
1. arguments.callee
2. window.onresize事件

## 开发步骤
1. 创建一个canvas区域
2. 在js中获得canvas区域
3. 创建一个rain类
4. rain中有初始化方法init()
5. rain中有画图方法draw()
6. rain中有移动方法move()
7. 在rain移动的时候，给canvas添上一个透明度，用来欺骗用户，以为是雨滴落下
8. 在rain落到底部的时候，让rain变成一个圆，并放大
9. 调用rain的init()，从头再来
