<template>
	<div>
		
		<div class="pd30 pr">
			<!-- 数据标注 -->
			<div class="dataStats_tag fs12" style="width: 100px; position: absolute; top: 10px;left: 15px;">
				<p class="item flex"><em class="dian C-one"></em>总邀约</p>
				<p class="item flex"><em class="dian C-two"></em>总面试</p>
				<p class="item flex"><em class="dian C-three"></em>总消费</p>
				<p class="item flex"><em class="dian C-four"></em>总进账</p>
			</div>
			
			<!-- 数据统计 -->
			<div class="dataStats_Head flexCenter pr fs13">
				<div class="fx_item one center">
					<span class="text">22人</span>
				</div>
				<div class="fx_item two center">
					<span class="text">20人</span>
				</div>
				<div class="fx_item three center">
					<span class="text">100元</span>
				</div>
				<div class="fx_item four center">
					<span class="text">200元</span>
				</div>
			</div>
		</div>
		
		<div class="pdlr4 f5bj flexRowBetween pdtb10 timeNav">
			<div class="item flexColumn">
				<p class="fs13 flexCenter">开始时间<img class="icon" src="../../static/images/statistics-icon.png" ></p>
				<p class="fs12 color6">2019.11.14</p>
			</div>
			<div class="item flexColumn">
				<p class="fs13 flexCenter">结束时间<img class="icon" src="../../static/images/statistics-icon.png" ></p>
				<p class="fs12 color6">2019.11.14</p>
			</div>
		</div>
		
		<div class="pdlr4 dataStats_infor mgb30">
			<div class="item flexRowBetween pdtb10 bordB1" v-for="item in dataStats">
				<h1 class="name ftw">张丹</h1>
				<p class="cont flexRowBetween fs13">
					<span class="child flex"><em class="dian C-one"></em>已邀约：5人</span>
					<span class="child flex"><em class="dian C-two"></em>已面试：5人</span>
					<span class="child flex"><em class="dian C-three"></em>已消费：5人</span>
					<span class="child flex"><em class="dian C-four"></em>已进账：5人</span>
				</p>
			</div>
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
				dataStats:[{},{},{}]
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
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
	@import "../../assets/style/dataStats.css";
	
</style>

