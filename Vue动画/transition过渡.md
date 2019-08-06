## transition
transition一般用来做 **进入/离开** 的过渡<br>
首先需要用```<transition name="xxx"></transition>```包裹需要过渡的组件或元素
### 相关类名
下面的前缀和name值对应
- .fade-enter: 元素开始插入的第一帧的状态, 第一帧结束后被删除
- .fade-enter-active: 定义过渡生效的状态, 整个过渡过程都有效
- .fade-enter-to: 元素插入的过渡动画的最后一帧, 过渡完成后被删除, **一般不用定义, 和元素显示时的常态一致即可**
- .fade-leave: 开始移除的第一帧, **一般不用定义, 和元素显示时的常态一致即可**
- .fade-leave-active: 移除过程状态
- .fade-leave-to: 移除结束前的最后一帧
```
.fade-enter-active, .fade-leave-active {
  transition: opacity 10s;
}
.fade-enter, .fade-leave-to{
  opacity: 0.3;
}
```

**注意: 如果不定义.fade-enter-to和.fade-leave, 需要过渡的属性必须有一个常态值, 否则会无效**<br>
如上的opacity虽然没有定义两个类默认, 但是opacity默认初始值是1<br>
比如: 我要过渡width属性, 则必须设置一个width的常态值(即过渡结束后的值), 否则就必须设置上述两个类名里对应的值
