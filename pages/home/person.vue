<template>
	<view>
		<view class="nav" style="position: sticky;top: 0px;left: 0px;z-index: 5;">
			<view class="left" @click="sz">
				<image src="../../static/img/sz.png" class="left1"></image>
			</view>
			<view class="right" @click="xx">
				<image src="../../static/img/xx.png" class="right1"></image>
			</view>
		</view>
		<view class="top">
			<view class="top1">
				
			</view>
			<view class="top2">
				<image src="../../static/img/tx.png" mode=""></image>
				<button @click="login" v-show="!flag">登录/注册</button>
				<view class="vs" v-show="flag">
					用户名:{{username}}
				</view>
			</view>
			
		</view>
		<view class="body">
			<view class="body1">
				<image src="../../static/img/qb.png" mode=""></image><br>
				我的钱包</view>
			<view class="body2">0<br>红包</view>
			<view class="body2">0<br>优惠卷</view>
			<view class="body2">0<br>白条</view>
			<view class="body2">0<br>鲜豆</view>
		</view>
		<view class="img">
			<swiper :autoplay="true" :interval="1000" :circular="true">
				<swiper-item>
					<view style="background-color: #0000FF;height: 100upx;line-height: 100upx;"><image src="../../static/img/lb1.JPG" mode="" class="img1"></image></view>
				</swiper-item>
				<swiper-item>
					<view style="background-color: #fff333;height: 100upx;line-height: 100upx;"><image src="../../static/img/lb2.JPG" mode="" class="img1"></image></view>
				</swiper-item>
			 </swiper>
		</view>
		<view class="bottom">
			<view class="bottom1"><image src="../../static/img/xin.png" mode=""></image><br>我的关注</view>
			<view class="bottom1"><image src="../../static/img/pj.png" mode=""></image><br>我的评价</view>
			<view class="bottom1"><image src="../../static/img/dz.png" mode=""></image><br>我的地址</view>
			<view class="bottom1"><image src="../../static/img/kb.png" mode=""></image><br>我的卡包</view>
			<view class="bottom1"><image src="../../static/img/hbm.png" mode=""></image><br>红包套餐</view>
			<view class="bottom1"><image src="../../static/img/hb.png" mode=""></image><br>我的奖励金</view>
			<view class="bottom1" @click="qd"><image src="../../static/img/qd.png" mode=""></image><br>签到有惊喜</view>
			<view class="bottom1"><image src="../../static/img/sh.png" mode=""></image><br>退款/售后</view>
			<view class="bottom1"><image src="../../static/img/kf.png" mode=""></image><br>客服反馈</view>
			<view class="bottom1"><image src="../../static/img/d.png" mode=""></image><br>帮助中心</view>
			<view class="bottom1"><image src="../../static/img/yhzc.png" mode=""></image><br>配送员注册</view>
			<view class="bottom1"><image src="../../static/img/pb.png" mode=""></image><br>达达同城送</view>
			<view class="bottom1"><image src="../../static/img/zs.png" mode=""></image><br>金融权益</view>
			<view class="bottom1"><image src="../../static/img/h.png" mode=""></image><br>掌声有礼</view>
			<view class="bottom1"><image src="../../static/img/yxz.png" mode=""></image><br>浦发有礼</view>
		</view>
	</view>
	
</template>

<script>
	import uniNavBar from "@dcloudio/uni-ui/lib/uni-nav-bar/uni-nav-bar.vue"
export default {
    components: {uniNavBar},
		data() {
		return {
			username:'',
			flag:false
		}
	},
	methods: {
		qd(){
			uni.navigateTo({
				url:"../person/qd"
			})
		},
		login(){
			uni.navigateTo({
				url:"../person/login"
			})
		},
		sz(){
			uni.navigateTo({
				url:"../person/sz"
			})
		},
		xx(){
			uni.navigateTo({
				url:"../person/xx"
			})
		},
		pd(){
			if(this.username==''){
				this.flag=false
			}
		}
	},
	mounted(){
		uni.getStorage({
			key: 'baseUser',
			success:(res)=>{
				this.username=res.data.username
				this.flag=true
			},
		});
		this.pd();
	}
}
</script>

<style>
	@import url("../../static/css/person.css");
</style>
