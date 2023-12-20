<template>
	<view>
		<button type="primary" @click="showActionSheet1()">点击显示操作菜单1</button>
		<button type="primary" @click="showActionSheet2()">点击显示操作菜单2</button>
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
				})
			},
			showActionSheet2() {
				uni.showActionSheet({
					itemList: (function() {
						const data = [];
						for (var i = 0; i < 100; i++) {
							data.push('按钮' + (i + 1));
						}
						return data;
					}())
				})
			}
		}
	}
</script>

<style>
	button {
		margin: 10px;
	}
</style>