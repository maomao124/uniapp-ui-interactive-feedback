<template>
	<view>
		<button type="primary" @click="toast1">普通toast</button>
		<button type="primary" @click="toast2">success toast</button>
		<button type="primary" @click="toast3">error toast</button>
		<button type="primary" @click="toast4">fail toast</button>
		<button type="primary" @click="toast5">exception toast</button>
		<button type="primary" @click="toast6">loading toast</button>
		<button type="primary" @click="toast7">none toast</button>
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
					icon:'success',
					title:'测试'
				})
			},
			toast3()
			{
				uni.showToast({
					icon:'error',
					title:'测试'
				})
			},
			toast4()
			{
				uni.showToast({
					icon:'fail',
					title:'测试'
				})
			},
			toast5()
			{
				uni.showToast({
					icon:'exception',
					title:'测试'
				})
			},
			toast6()
			{
				uni.showToast({
					icon:'loading',
					title:'测试'
				})
			},
			toast7()
			{
				uni.showToast({
					icon:'none',
					title:'测试'
				})
			}
		}
	}
</script>

<style>
button{
	margin: 10px;
}
</style>
