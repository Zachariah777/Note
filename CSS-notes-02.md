# CSS 知识总结

## 浏览器的渲染原理
1. 处理 HTML 标记并构建 DOM 树。
2. 处理 CSS 标记并构建 CSSOM 树。
3. 将 DOM 与 CSSOM 合并成一个渲染树。
4. Layout 布局（文档流、盒模型、计算大小和位置）
5. Paint 布局（把边框颜色、文字颜色、阴影等画出来）
6. Compose 合成（根据层叠关系展示画面）
***
## CSS CSS 动画的两种做法（transition 和 animation）

&emsp;&emsp;transition 过渡可以为一个元素在不同状态之间切换的时候定义不同的过渡效果。transition的属性有transition-property（css属性name）、transition-duration（动画持续时间）、transition-timing-function（动画的变化过程速度曲线）、transition-delay（动画延迟时间）<br>

`transiton: 过渡属性 过渡时间 过渡动画函数 过渡延迟时间；`<br>

&emsp;&emsp;而animation属性可以像Flash制作动画一样，通过控制关键帧来控制动画的每一步，实现更为复杂的动画效果。<br>

`animation: 动画时间 过渡方式 动画延迟 动画循环次数 动画方向 动画时间外的属性 是否暂停 动画名字`<br>

（1）animation-name：none为默认值，将没有任何动画效果，其可以用来覆盖任何动画<br>
（2）animation-duration：默认值为0，意味着动画周期为0，也就是没有任何动画效果<br>
（3）animation-timing-function：与transition-timing-function一样<br>
（4）animation-delay：在开始执行动画时需要等待的时间<br>
（5）animation-iteration-count：定义动画的播放次数，默认为1，如果为infinite，则无限次循环播放<br>
（6）animation-direction：默认为nomal，每次循环都是向前播放，（0-100），另一个值为alternate，动画播放为偶数次则向前播放，如果为基数词就反方向播放<br>
（7）animation-state：默认为running，播放，paused，暂停<br>
（8）animation-fill-mode：定义动画开始之前和结束之后发生的操作，默认值为none，动画结束时回到动画没开始时的状态；forwards，动画结束后继续应用最后关键帧的位置，即保存在结束状态；backwards，让动画回到第一帧的状态；both：轮流应用forwards和backwards规则。<br>

## &emsp;&emsp;两者的主要区别在于：transition需要触发一个事件才会随着时间改变其CSS属性；animation在不需要触发任何事件的情况下，也可以显式的随时间变化来改变元素CSS属性。