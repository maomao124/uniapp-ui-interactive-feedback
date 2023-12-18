<template>
	<view>
		<button type="primary" @click="showModal1">showModal</button>
		<button type="primary" @click="showModal2">showModal 无取消按钮</button>
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
					showCancel:false,
					title:'提示',
					content:'提示内容。。。。。。。。。。。。。'
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
