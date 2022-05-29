<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		 <u-button>按钮</u-button>
		 <u-button type="success">成功按钮</u-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		async onLoad() {
			// this.$u.get('/api/index').then(res => {
			// 	console.log(res)
			// })
			
			//await 必须写在async 函数中
			// const res = await this.$u.get('/api/index')
			// console.log(res)
			// console.log(22)
			const res = await this.$u.post('/api/auth/login')
			console.log(res)
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
