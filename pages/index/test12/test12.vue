<template>
	<view>
		<button type="primary" @click="showModal1">showModal</button>
		<button type="primary" @click="showModal2">showModal 输入框</button>
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
					editable:true,
					placeholderText:'请输入文字',
					title:'提示',
					//content:'提示内容。。。。。。。。。。。。。',
					success: (data) => {
						console.log(data);
						if(data.confirm)
						{
							console.log("选择了确定");
							console.log("文字内容：",data.content);
						}
						if(data.cancel)
						{
							console.log("选择了取消");
						}
					},
					fail: (err) => {
						console.log("错误：",err);
					}
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
