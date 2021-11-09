<template>
	<view class="content color">
		<image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
			<button type="default" @click="open">打开新页面</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		// 监听页面加载
		onLoad() {
			console.log('page onload');
			uni.getSystemInfo({
				success(res) {
					console.log(res);
				},
				fail(err) {
					console.log(err)
				},
				complete(res) {
					console.log('finally come here')
				}
			})
		},
		// 监听页面初次渲染完成
		onReady() {
			console.log('page onready');
		},
		// 监听页面显示
		onShow() {
			console.log('page onshow');
		},
		onHide() {
			console.log('page onhide');
		},
		onUnload() {
			console.log('page onunload');
		},
		methods: {
			open(){
				uni.navigateTo({
					url:'../test-a/test-a'
				})
			}
		}
	}
</script>

<style>
	@import './index.css';
	page {
		background-color: #007AFF;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin: 200rpx auto 50rpx auto;
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
