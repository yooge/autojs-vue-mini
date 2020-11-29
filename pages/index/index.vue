<template>
	<view>
	 
		<form>
			
			 <view class="padding flex flex-direction">
			 	<button class="cu-btn bg-green shadow margin-tb-sm lg"  @click="start"> 启动朋友圈骚扰 </button>
			 	<button class='cu-btn bg-green shadow' @click="stop">停止</button>
			 </view>
			  
		</form>
		 
	</view>
	
</template>

<script>

	var {robot} = require('robot-tools');
	
	export default {
		 
		methods: {
			start() {
				 robot.stop(); 
				 var param = {  
					 file: 'robot.weixin.js', 
				 }
				 console.log("start");  
				 robot.start(param);
			},
			stop() {
				 robot.stop();
			}
			 
		}
	}
</script>
 