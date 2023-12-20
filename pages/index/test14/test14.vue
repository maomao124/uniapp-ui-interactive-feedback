<template>
	<view>
		<button type="primary" @click="showActionSheet1()">点击显示操作菜单1</button>
		<button type="primary" @click="showActionSheet2()">点击显示操作菜单2 - 红色</button>
		<button type="primary" @click="showActionSheet3()">点击显示操作菜单2 - 蓝色</button>
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
					itemList: ['a', 'b', 'c'],
					itemColor:'#ff0000'
				})
			},
			showActionSheet3() {
				uni.showActionSheet({
					itemList: ['a', 'b', 'c'],
					itemColor:'#00aaff'
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