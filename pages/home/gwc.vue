<template>
	<view>
		<view class="nav">
			<view class="left">我的购物车</view>
			<view class="right">
				<image src="../../static/img/xing.png" class="right1"></image>
			</view>
		</view>
			<view class="content">
				
				<view class="gouwuche">
						<view class="gouwuche1">
							<text>口红一号铺</text>
						</view>
						<view class="tupian">
							<image src="../../static/img/cw2.png" mode=""></image>
						</view>
				</view>
				<view class="gouwuche2">
						<view class="gouwuche3">
							<text>口红一号铺</text>
						</view>
						<view class="tupian2">
							<image src="../../static/img/cw2.png" mode=""></image>
						</view>
				</view>
			</view>
	</view>
</template>

<script>
	export default {
	    data() {
	        return {
	          
	        }
		},
	    methods: {

	       }
	    }

</script>

<style>
	.nav{
		height: 50px;
		width: 100%;
		background: #48C23D;
	}
	.left{
		height: 20px;
		padding-top: 20px;
		width: 60%;
		float: left;
		text-align: right;
		color: white;
	}
	.right{
		height: 20px;
		padding-top: 20px;
		width: 40%;
		float: right;
	}
	.right1{
		height: 20px;
		width: 20px;
		margin-left: 78%;
	}
	.content {
		width: 100%;
		text-align: center;
		height: 500px;
		background-color: #F5F5F5;
	}
	.dingwei{
		width: 400upx;
		height: 50upx;
		border: 10upx solid #B4EEB4;
		border-radius: 50upx;
		position: absolute;
		left: 70px;
		top: 28px;
	}
	.dingwei2{
		width: 100%;
		height: 100%;
		background-color: #71C671;
		border-radius: 50upx;
	}
	.dingwei2 image{
		width: 35upx;
		height: 35upx;
		position: absolute;
		left: 10px;
		top: 3px;
	}
	.dingwei2 text{
		font-size: 30upx;
		color: white;
		position: absolute;
		left: 30px;
		top: 3px;
	}
	.gouwuche{
		width: 93%;
		height: 300upx;
		position: absolute;
		left: 13px;
		top: 70px;
		background-color: white;
		border-radius: 20upx;
	}
	.gouwuche1{
		width: 100%;
		height: 85upx;
		position: absolute;
		left: 0px;
		top: 0px;
		background-color: #9BCD9B;
		border-radius: 20upx 20upx 0 0;
	}
	.gouwuche1 text{
		font-size: 40upx;
		color: white;
		position: absolute;
		left: 10px;
		top: 7px;
	}
	.tupian image{
		width: 150upx;
		height: 150upx;
		border-radius: 20upx;
		position: absolute;
		left: 10px;
		top: 50px;
	}
	.gouwuche2{
		width: 93%;
		height: 300upx;
		position: absolute;
		left: 13px;
		top: 220px;
		background-color: white;
		border-radius: 20upx;
	}
	.gouwuche3{
		width: 100%;
		height: 85upx;
		position: absolute;
		left: 0px;
		top: 0px;
		background-color: #9BCD9B;
		border-radius: 20upx 20upx 0 0;
	}
	.gouwuche3 text{
		font-size: 40upx;
		color: white;
		position: absolute;
		left: 10px;
		top: 7px;
	}
	.tupian2 image{
		width: 150upx;
		height: 150upx;
		border-radius: 20upx;
		position: absolute;
		left: 10px;
		top: 50px;
	}
</style>
