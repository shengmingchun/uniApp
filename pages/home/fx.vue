<template>
	<view>
		<view class="nav">
			<view class="left">发现</view>
			<view class="right">
				<image src="../../static/img/xing.png" class="right1"></image>
			</view>
			<view style="position: sticky;top: auto;left: 0px;z-index: 5;">
				<wuc-tab :tab-list="items" :tabCur.sync="current" @change="onClickItem" 
				:textFlex="true" 
				tabStyle="color:white;font-size:15px;"
				 selectClass="text-white" 
				 >
				</wuc-tab>
			</view>
			
		</view>
		<view>
			<view style="height: 40px;width: 100%;"></view>
			  <view class="content">
			    <view v-show="current === 0">
					 <one></one>
			    </view>
			    <view v-show="current === 1">
			       <tow></tow>
			    </view>
			    <view v-show="current === 2">
			        <tj></tj>
			    </view>
				<view v-show="current === 3">
				   <ssmz></ssmz>
				</view>
				<view v-show="current === 4">
				  <sh></sh>
				</view>
			</view>
		</view>
	</view>
	
</template>

<script>
import WucTab from '@/components/wuc-tab/wuc-tab.vue';
import one from '../fx/one.vue'
import tow from '../fx/tow.vue'
import tj from '../fx/tj.vue'
import ssmz from '../fx/ssmz.vue'
import sh from '../fx/sh.vue'
export default {
    data() {
        return {
          items: [{name:'关注'},{name:'食谱'},{name:'推荐'},{name:'时尚美妆'},{name:'生活'}],
          current: 0,
        }},
    components: { WucTab,one,tow,tj,ssmz,sh},
    methods: {
        onClickItem(index) {
           if (this.current !== index) {
               this.current = index;
           }
       },
    }
}
</script>

<style>
.nav{
	height: 50px;
	width: 100%;
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
</style>
