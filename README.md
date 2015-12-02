# fbf.js
Produced a range of frame by frame animation of javascript.
## frame-by-frame.js
这是一个用来产生css3逐帧动画的jQuery插件；<br>
依赖关系：jQuery<br>
支持回调函数，支持链式操作
<p>作者微博：<a href="http://weibo.com/u/1326039884">折腾笔记</a></p>
----------------
<span>目前版本0.0.4</span><br>
##下一版本改进目标：
1.配置开始结束帧改为可选参数；
2.默认改为不循环播放；
3.图片改为支持图片数组；
4.方法改为init()和play();
5.图片展示方式由背景改为图像；动画采用3D变换
##最简单的用法示例
<pre>
$('#fbf').fbf({
		img:'img/fbf.jpg',//图片地址
		start:0,//开始桢
		end:7//结束桢
});
</pre>
<p>图片的生成可以用这个<a href="http://pan.baidu.com/s/1o6Imtp4">图片拼接</a>工具<br>
导入全部图，横排即可</p>
##一个复杂示例
<pre>
$('#fbf').fbf({
		width:200,//舞台宽度默认元素宽度----->可选参数
		height:300,//舞台高度默认元素高度----->可选参数
		img:'img/fbf.jpg',//图片地址(如用相对路径请以实际发生动画的页面为准)----->必填
		frames:8,//总帧数，默认自动计算----->可选参数
		speed:100,//帧速，默认0.1秒----->可选参数
		loop:true,//循环，默认开启----->可选参数
		start:0,//开始帧，0为第一帧------------------------------->必填
		end:7,//结束帧,缺省为0------------------------------->必填
},function(){
alert('单次播放结束')；
});
</pre>
