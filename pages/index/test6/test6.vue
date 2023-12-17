<template>
	<view>
		<button type="primary" @click="toast1">显示toast</button>
		<button type="primary" @click="toast2">隐藏toast</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			toast1()
			{
				uni.showToast({
					duration:5000,
					title:'测试'
				})
			},
			toast2()
			{
				uni.hideToast();
			},
		}
	}
</script>

<style>
button{
	margin: 10px;
}
</style>
