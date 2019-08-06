## animation
### 类名定义动画
与transition一样, 只需在html中用```<transition>标签包裹, 加上name值```, <br>
然后用name值拼接动画类名: ```.name-enter-active```和 ```.name-leave-active```
```
.bounce-enter-active {
  animation: bounce-in .5s;
}
.bounce-leave-active {
  animation: bounce-in .5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```
### 使用第三方库的动画
只需在html标签上写入```enter-active-class```和```leave-active-class```, 对应第三方库动画的类名, 连name都可以省略了
