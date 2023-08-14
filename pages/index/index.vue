<template>
	<view class="sign_box">
		<!-- <up-button class="signbutton" text="登录"></up-button> -->
		<Signcpn></Signcpn>
	</view>
</template>

<script setup>
import { reactive } from 'vue';
const model1 = reactive({
	username: '',
	password: ''
});

const rules = reactive({
	username: {
		required: true,
		message: '请填写用户名',
		trigger: ['blur', 'change']
	},
	password: {
		required: true,
		message: '请填写密码',
		trigger: ['blur', 'change']
	}
});
</script>

<style scoped lang="scss">
.sign_box {
	width: 100vw;
	height: 100vh;
	position: relative;
	display: flex;
	justify-content: center;
	background-image: url(https://notebookbucket.oss-cn-hangzhou.aliyuncs.com/mobile/main_page/back.png);
	background-repeat: no-repeat;
	background-size: cover;
	.signbutton {
		width: 400rpx;
		height: 100rpx;
		border-radius: 50rpx;
		position: fixed;
		bottom: 300rpx;
	}
}
</style>
