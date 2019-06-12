<template>
	<view class="">
		<view class="top">
			<image src="../../static/img/tx.png" mode=""></image>
		</view>
		<view>
			<input type="text" v-model="username">
			<input type="password" v-model="password" v-if="fla">
			<input type="text" v-model="password" v-if="!fla">
			<view class="l1">
				<uni-icon type="eye" size="30" @click="fn"></uni-icon>
			</view>
			<button type="primary" @click="login">登录</button>
			<button type="primary" @click="register">注册</button>
		</view>
	</view>
</template>

<script>
import uniIcon from '@dcloudio/uni-ui/lib/uni-icon/uni-icon.vue'
export default {
	components: {uniIcon},
	data() {
		return {
			username:'smc',
			password:'123456',
			fla:true,
		}
	},
	methods: {
		register(){
			uni.navigateTo({
				url: 'register'
			});
		},
		login(){
			if(this.username.length<=0){
				uni.showToast({
					title: '请输入用户名',
					duration: 2000,
					
				});
				return;
			}
			if(this.password.length<=0){
				uni.showToast({
					title: '请输入密码',
					duration: 2000,		
				});
				return ;
			}
			if(this.password=="123456" && this.username=="smc"){
				uni.setStorage({
					key: 'baseUser',
					data: {username:this.username,password:this.password}
				});
				uni.reLaunch({
					url: '../home/person'
				})
			}		
		},
		fn(){
			this.fla=!this.fla;
		}
	},
}
</script>

<style>
		@import url("../../static/css/login.css");
</style>
