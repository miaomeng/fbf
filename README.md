# fbf.js
Produced a range of frame by frame animation of javascript.
##  frame-by-frame.js
这是一个用来产生css3逐帧动画的插件；<br>
依赖关系：jQuery<br>
<p>作者微博：<a href="http://weibo.com/u/1326039884">折腾笔记</a></p>
----------------
<span>目前版本0.0.5</span><br>

## 最简单的用法示例
初始化
<pre>
var $fbf = new FBF('#fbf', {
	img: 'img/fbf.jpg',
});
</pre>
播放
<pre>
$fbf.play();
</pre>
<p>图片的生成可以用这个<a href="https://github.com/zhetengbiji/img-Splice">图片拼接</a>工具<br>
导入全部图，横排即可</p>
## 一个最复杂示例
初始化
<pre>
var $fbf = new FBF('#fbf', {
	width: 200, //舞台宽度默认元素宽度------->可选参数
	height: 300, //舞台高度默认元素高度------->可选参数
	img: 'img/fbf.jpg', //图片地址(如用相对路径请以实际发生动画的页面为准)------------------------------->必填
	frames: 8, //总帧数，默认自动计算------->可选参数
	speed: 100, //帧速，默认0.1秒------->可选参数
	loop: true, //循环，默认关闭------->可选参数
	start: 0, //开始帧，0为第一帧------->可选参数
	end: 7, ////结束帧,缺省为最后一帧------->可选参数
});
</pre>
播放
<pre>
//	倒序播放
$fbf.play({
	start: 7,
	end: 0,
}, function() {
	console.log('播放完毕');
});
</pre>

## 下一版本改进目标：
1. 图片改为支持图片数组或者竖排序列帧；
2. 图片展示方式由背景改为图像；动画采用3D变换
