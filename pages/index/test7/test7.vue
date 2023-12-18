<template>
	<view>
		<button type="primary" @click="loading1">showLoading</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			loading1()
			{
				uni.showLoading({
					title:'加载中，请稍后...'
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
