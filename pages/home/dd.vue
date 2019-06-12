<template>
	<view>
		<view class="nav">
			<view class="left">我的订单</view>
			<view class="right">
				<image src="../../static/img/xing.png" class="right1"></image>
			</view>
		</view>
		<view class="top">
			<image src="../../static/img/dd.jpg"></image>
			<button>去逛逛</button>
		</view>
	
	</view>
</template>

<script>
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
	.top{
		margin: 40px auto;
	}
	.top image{
		width: 100%;
		height: 180px;
	}
	button{
		width: 30%;
		height: 30px;
		background: #3F9DFF;
		line-height: 30px;
	}
</style>
