<template>
	<view>
		<button type="primary" @click="toast1">普通toast</button>
		<button type="primary" @click="toast2">position top toast</button>
		<button type="primary" @click="toast3">position center toast</button>
		<button type="primary" @click="toast4">position bottom toast</button>
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
					position:'top',
					title:'测试'
				})
			},
			toast3()
			{
				uni.showToast({
					position:'center',
					title:'测试'
				})
			},
			toast4()
			{
				uni.showToast({
					position:'bottom',
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
