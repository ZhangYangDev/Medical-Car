<template name="page-foot">
	<view class="page-share-title">
		<text>{{name}}若您的手机号未注册，将为您自动注册。注册或登录即代表您同意我们的</text>
		<text class="submit" @tap="submit">服务协议</text>和<text class="submit" @tap="submit">隐私政策</text>。
	</view>
</template>

<script>
	export default {
		name: "page-foot",
		props: {
			name: {
				type: String,
				// default: "上海连为科技有限公司"
			}
		},
		methods: {
			submit() {
				uni.showModal({
					content:"hello uni-app开源地址为https://github.com/dcloudio/uni-app/tree/master/examples，请在这个开源项目上贡献你的代码",
					showCancel:false
				})
			}
		}
	}
</script>
<style>
	.page-share-title {
		text-align: center;
		font-size: 30rpx;
		color: #BEBEBE;
		padding: 20rpx 0;
	}

	.submit {
		border-bottom: 1rpx solid #BEBEBE;
	}
</style>
