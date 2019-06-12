<template>
	<view class="content">
		<view class="nav">
			<view class="left">
				<image src="../../static/img/dw.png" class="left1"></image>
				北京市
				<image src="../../static/img/xxjt.png" class="left2"></image>
			</view>
			<view class="right">
				<image src="../../static/img/erweima.png" class="right1"></image>
			</view>
		</view>
		<view class="top">
			<view class="top1">
				<view class="top2" @click="search">
					<image src="../../static/img/fdj.png" mode=""></image>
					<view class="top3">酸奶</view>
				</view>
			</view>
			<view class="top4">
				<ul v-for="obj in arr" :key="obj">
					<li>{{obj}}</li>
				</ul>
			</view>
			<view id="top4">
				<image src="../../static/img/top.jpg" mode=""></image>
			</view>
			<view class="top5">
				<view class="top6">
					<view class="top7">超</view>
					<view class="top8">超市便利</view>
				</view>
				<view class="top6">
					<view class="top7">级</view>
					<view class="top8">生鲜果蔬</view>
				</view>
				<view class="top6">
					<view class="top7">品</view>
					<view class="top8">烘培蛋糕</view>
				</view>
				<view class="top6">
					<view class="top7">牌</view>
					<view class="top8">鲜花绿植</view>
				</view>
				<view class="top6">
					<view class="top7">周</view>
					<view class="top8">医药健康</view>
				</view>
				<view class="top6">
					<view class="top7">秒</view>
					<view class="top8">家居时尚</view>
				</view>
				<view class="top6">
					<view class="top7">杀</view>
					<view class="top8">限时抢卷</view>
				</view>
				<view class="top6">
					<view class="top7">1</view>
					<view class="top8">签到</view>
				</view>
				<view class="top6">
					<view class="top7">元</view>
					<view class="top8">大牌福利</view>
				</view>
				<view class="top6">
					<view class="top7">起</view>
					<view class="top8">0元抽奖</view>
				</view>
			</view>
			<view class="top9">
				<image src="../../static/img/top2.jpg" mode=""></image>
			</view>
		</view>
		
	</view>
</template>

<script>
		
	export default {
	   
			data() {
			return {
				arr:["妇炎胶囊","牛奶","咽喉","清热","健脾","啤酒","小熊饼干"],
			}
		},
		methods: {
			search(){
				uni.navigateTo({
					url:"../index/search"
				})
			}
		}
	}
</script>

<style>
	@import url("../../static/css/index.css");
</style>
