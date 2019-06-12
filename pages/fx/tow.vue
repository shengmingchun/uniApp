<template>
	<viw>
		<image src="../../static/img/fx01.jpg" mode="" class="i1"></image>
		<view class="top">
			<view class="top1">
				<view class="top2" @click="search">
					<image src="../../static/img/fdj.png" mode=""></image>
					<view class="top4"> 搜索名 食材</view>
				</view>
			</view>
			<view class="top3">
			关注门店，获取最新优惠信息~
			</view>
		</view>
		<view class="body">
			<view class="body1"></view>
			<view class="body2">
				<view class="body4">附近食谱</view>
			</view>
			<view  class="img1">
				<image src="../../static/img/fx01.jpg" mode=""></image>
				<text>鱼香肉丝</text>
			</view>
			<view  class="img1">
				<image src="../../static/img/fx01.jpg" mode=""></image>
				<text>鱼香肉丝</text>
			</view>
			<view  class="img1">
				<image src="../../static/img/fx01.jpg" mode=""></image>
				<text>鱼香肉丝</text>
			</view>
		</view>
	</viw>
</template>

<script>
	export default {
	   
			data() {
			return {
				
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
	@import url("../../static/css/tow.css");
</style>
