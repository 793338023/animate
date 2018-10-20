# animate
运动
例子:
 var anmimate = new Animator({
	targetVal:100,
	curVal:100,
	step:0.6,
	point:2,
	easeType:'Quad-easeInOut',
	update:function(val){
		oEl.style.left = val + 'px';
	},
	complete:function(){
		console.log('complete...');
	}
});
anmimate.start(); //启动
参数有:
 * targetVal 目标数字
 * curVal 起始点
 * step 运动时间 (秒)
 * point 保留数字位数
 * easeType 运动缓冲类型
 * update 每次运动更新
 * complete 运动完成
 
 而easeType需要根据Tween里的属性名，格式时属性名-属性名找到对应的方法，如
 Quad-easeIn
 Cubic-easeIn
 
 它的所有运动都在update里，update会返回当前运动的数字，然后根据它在update里编写运动物体。
 
 
  
