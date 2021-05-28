`resetgame`控制整个重启(重绘)



在animate中通过



开始的介绍通过透明度来显示与隐藏

这里

```
1.css
	transition:opacity 2s（控制这个改变时间）
2.js
	由游戏开始的鼠标点击事件设置opacity，retgame里设置opacity
	opacity是一个控制透明度的属性，1为不透明，0为全透明
```



鼠标监听按下事件

```javascript
window.requestAnimationFrame(animate);
//告诉浏览器——你希望执行一个动画，并且要求浏览器在下次重绘之前调用指定的回调函数更新动画。该方法需要传入一个回调函数作为参数，该回调函数会在浏览器下一次重绘之前执行
```

mouseup监听事件

`heating = false`用来控制animate中的条件



animate作为游戏的主要控制（绘图）代码段

当在加热状态时

`window.requestAnimationFrame(animate);`程序的末尾有该函数，如果判断游戏失利则return不执行该语句。
