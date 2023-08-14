<template>
	<view class="signbox">
		<view class="signinnerbox">
			<view class="signuser_box">
				<up-input fontSize="18" placeholder="请输入账号" border="surround" v-model="value" @change="change"></up-input>
			</view>
			<view class="signpwd_box">
				<up-input
					fontSize="18"
					suffixIcon="eye-off"
					suffixIconStyle="font-size: 22px;color: black"
					placeholder="请输入密码"
					border="surround"
					v-model="value"
					@change="change"
				></up-input>
				<view class="singbtn"></view>
			</view>
			<up-button class="signButton" type="primary" text="登录"></up-button>
		</view>
	</view>
</template>

<script>
export default {
	name: 'Signcpn',
	data() {
		return {};
	}
};
</script>

<style scoped lang="scss">
.signbox {
	position: fixed;
	width: 700rpx;
	height: 600rpx;
	// background-color: white;
	border-radius: 50px;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	background-color: white;
	display: flex;
	align-items: center;
	justify-content: center;
	.signuser_box {
		width: 600rpx;
		height: 110rpx;
		display: flex;
		align-items: center;
		margin-bottom: 21px;
		background-color: #f4f4f4;
		border-radius: 50px;
		padding-left: 20px;
		box-sizing: border-box;
	}
	.signpwd_box {
		width: 600rpx;
		height: 110rpx;
		display: flex;
		align-items: center;
		background-color: #f4f4f4;
		border-radius: 50px;
		margin-bottom: 21px;
		padding-left: 20px;
		padding-right: 10px;
		box-sizing: border-box;
		position: relative;
		.singbtn {
			width: 80rpx;
			height: 80rpx;
			position: absolute;
			bottom: 0;
			right: 0;
			background-color: transparent;
			border: none !important;
		}
	}
	.signButton {
		width: 600rpx;
		border-radius: 50rpx;
		height: 100rpx;
		background-color: #ff93dd;
		border: none;
		font-size: 16px;
		font-weight: 600;

		::v-deep .u-button__text {
			font-size: 16px !important;
		}
	}
}
</style>
