<template>
	<view>
		<button type="primary" @click="toast1">普通toast</button>
		<button type="primary" @click="toast2">duration 3000 toast</button>
		<button type="primary" @click="toast3">duration 5000 toast</button>
		<button type="primary" @click="toast4">duration 500 toast</button>
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
					duration:3000,
					title:'测试'
				})
			},
			toast3()
			{
				uni.showToast({
					duration:5000,
					title:'测试'
				})
			},
			toast4()
			{
				uni.showToast({
					duration:500,
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
