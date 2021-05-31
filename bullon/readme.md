- `resetgame`控制整个绘图参数的初始化（和还原）

- `draw()`函数负责页面绘制（[*HTML*5 Canvas](http://www.baidu.com/link?url=Wl0AeeY2Eiak8e7YBagikEOo_E9kY_kGuKbHLlynCzcHze3IkyFZCjctZAqNfOpPe4M88b_9Ycg00Bia7q8jSK)）
- 监听事件：`mousedown、up、resize、keydown`
- `animate`是游戏主循环函数，控制运动参数使绘图参数变化





开始的介绍画面通过透明度来显示与隐藏

这里的知识点：

```
1.css
	transition:opacity 2s（控制这个改变时间）
2.js
	由游戏开始的鼠标点击事件设置opacity，retgame里设置opacity
	opacity是一个控制透明度的属性，1为不透明，0为全透明
```



## 监听事件

#### mousedown

```javascript
window.requestAnimationFrame(animate);
//告诉浏览器——你希望执行一个动画，并且要求浏览器在下次重绘之前调用指定的回调函数更新动画。该方法需要传入一个回调函数作为参数，该回调函数会在浏览器下一次重绘之前执行
```

#### mouseupCancel changes

与mousedown配合来控制`heating`的值，为布尔量，当true时animate中会控制热气球的改变。





## animate

游戏主循环函数，控制运动参数使绘图参数变化

- 在animate中通过碰撞规则来判定是否继续游戏，若继续则

  `window.requestAnimationFrame(animate);`程序的末尾有该函数，如果判断游戏失利则return不执行该语句。

- 加热布尔量

  改变速度，从而改变balloonXY值，在draw中重绘图像

- hitDetection

  通过欧氏距离检测碰撞

## Resetgame

- 控制游戏开始（隐藏按钮介绍等）`opacity属性`

- 生成树与背景树

  生成的数据放在数组中，送入后续的draw中

## draw

用于画图的核心函数
