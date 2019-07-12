1. Vue用对象语法动态绑定className时，对象属性名如果需要用到模板字符串,需要用[]包裹
```
<button :class="[{[`icon-${iconPosition}`]: true},'class1','class2']"
```
2. 对象语法简写
```
<input :class="{'error': error}"> => <input :class="{error}">
```
