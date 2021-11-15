<template>
	<view>
		<view class="loginBox">
			账号：<input type="text" v-model="username"class="username"/>
		</view>
		<view class="loginBox">
			密码：<input type="number" v-model="password" class="password"/>
		</view>
			<button @click="login('login')">登录</button>
			<button @click="login('register')">注册</button>
	</view>
</template>

<script>
	export default {
		name: "Index",
		data() {
			return {
				isLogin: true,
				username: '',
				password: '',
			}
		},
		methods: {
			login(type) {
				if(type == "login") {
					console.log("登录");
				}else {
					console.log("注册");
				}
			}
		}
	}
</script>

<style scoped>
	.loginBox {
		display: flex;
		margin: 20px 0px;
	}
	.username , .password{
		width: 70%;
		border:1px solid red;
	}
</style>
