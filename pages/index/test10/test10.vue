<template>
	<view>
		<button type="primary" @click="showModal1">showModal</button>
		<button type="primary" @click="showModal2">showModal 自定义按钮文字</button>
		<button type="primary" @click="showModal3">showModal 自定义按钮颜色</button>
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
					cancelText:'否',
					confirmText:'是',
					title:'提示',
					content:'提示内容。。。。。。。。。。。。。'
				})
			},
			showModal3()
			{
				uni.showModal({
					cancelText:'否',
					confirmText:'是',
					cancelColor:'#dd524d',
					confirmColor:'#00ff00',
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
