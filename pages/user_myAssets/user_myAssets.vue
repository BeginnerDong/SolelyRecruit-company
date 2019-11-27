<template>
	<div>
		
		<div class="pdlr4 mgtb20">
			<div class="assets_Head flexCenter  pr">
				<div class="cont center">
					<p class="fs13 color6 mgb5">余额</p>
					<p class="fs16">1500</p>
				</div>
				<img class="fixdata" src="../../static/images/statistics-icon1.png"/>
				
				<div class="xfMny fs12 pa">消费：500</div>
				<div class="czMny fs12 pa">充值：2000</div>
			</div>
			
			<div class="flexCenter assets_seltbtn center fs13 pdt20">
				<span class="item" @click="Router.navigateTo({route:{path:'/pages/user_myAssets_recharge/user_myAssets_recharge'}})">充值</span>
				<span class="item mgl30" @click="Router.navigateTo({route:{path:'/pages/user_myCashOut/user_myCashOut'}})">提现</span>
			</div>
		</div>
		
		<div class="orderNav" style="background: #e0eeff;">
			<span class="tt" :class="num==1?'on':''" @click="change('1')">充值流水</span>
			<span class="tt" :class="num==2?'on':''" @click="change('2')">提现流水</span>
			<span class="tt" :class="num==3?'on':''" @click="change('3')">消费流水</span>
		</div>
		
		<div class="pdlr4 fs14" v-show="num==1">
			<ul>
				<li class="flexRowBetween pdtb15 bordB1" v-for="(item,index) in rechargNotes" :key="index">
					<span>2019.11.13</span>
					<span>+200</span>
				</li>
			</ul>
		</div>
		
		<div class="pdlr4 fs14" v-show="num==2">
			<ul>
				<li class="flexRowBetween pdtb15 bordB1" v-for="(item,index) in rechargNotes" :key="index">
					<span>2019.11.12</span>
					<span>-150</span>
				</li>
			</ul>
		</div>
		<div class="pdlr4 fs14" v-show="num==3">
			<ul>
				<li class="flexRowBetween pdtb15 bordB1" v-for="(item,index) in rechargNotes" :key="index">
					<span>2019.10.13</span>
					<span>-100</span>
				</li>
			</ul>
		</div>
		
		
	</div>
</template>


<script>
	export default {
		data() {
			return {
				Router:this.$Router,
				showView: false,
				is_show:false,
				num:1,
				rechargNotes:[{},{},{}]
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			change(num){
				const self = this;
				if(num!=self.num){
					self.num = num
				}
			},
			getMainData() {
				const self = this;
				const postData = {};
				postData.tokenFuncName = 'getProjectToken';
				var callback = function(res){
				    console.log('getMainData', res);
				    self.mainData.push.apply(self.mainData,res.info.data);		        
				};
				self.$apis.orderGet(postData, callback);
			}
		},
	}
</script>


<style>
	@import "../../assets/style/public.css";
	@import "../../assets/style/NavTab.css";
	
	.assets_Head{width: 150px;height: 150px;border:8px solid #0dbc84;margin: 0 auto;border-radius: 50%;box-sizing: border-box;}
	.assets_Head .xfMny{ left: 130px; top: 0px; min-width: 100px;}
	.assets_Head .czMny{right: 150px; top: 55px; min-width: 100px;text-align: right;}
	.assets_seltbtn .item{width: 75px; height: 30px;line-height: 30px;border-radius: 20px;border:1px solid #eee;}
	.fixdata{width: 75px;height: 75px; display: block; position: absolute; top: -8px;right:-8px;}
	
</style>

