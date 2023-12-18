<template>
	<view>
		<button type="primary" @click="showModal1">showModal</button>
		<button type="primary" @click="showModal2">showModal 事件</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			showModal1()
			{
				uni.showModal({
					title:'提示',
					content:'提示内容。。。。。。。。。。。。。'
				})
			},
			showModal2()
			{
				uni.showModal({
					title:'提示',
					content:'提示内容。。。。。。。。。。。。。',
					success: (data) => {
						console.log(data);
						if(data.confirm)
						{
							console.log("选择了确定");
						}
						if(data.cancel)
						{
							console.log("选择了取消");
						}
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
		}
	}
</script>

<style>
button{
	margin: 10px;
}
</style>
