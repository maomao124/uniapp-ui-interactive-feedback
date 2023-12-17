<template>
	<view>
		<button type="primary" @click="toast1">普通toast</button>
		<button type="primary" @click="toast2">透明蒙层 toast</button>
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
					title:'测试'
				})
			},
			toast2()
			{
				uni.showToast({
					mask: true,
					title:'测试'
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
