<template>
	<view>
		<button type="primary" @click="showActionSheet1()">点击显示操作菜单1 - 事件</button>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			showActionSheet1() {
				uni.showActionSheet({
					itemList: ['a', 'b', 'c'],
					success: (data) => {
						console.log('点击了第'+(data.tapIndex+1)+'个按钮');
					},
					fail: (err) => {
						console.log("失败的回调");
					},
					complete: () => {
						console.log("调用完成");
					}
				})
			},
		}
	}
</script>

<style>
	button {
		margin: 10px;
	}
</style>