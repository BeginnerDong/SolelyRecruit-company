<template>
	<div>
		
		<div class="editBetween pdlr4">
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>期望职位类型</span>
				<span class="flexEnd color6 fs13">会计<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>工作性质</span>
				<span class="flexEnd color6 fs13" @click="seltShow">全职<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>期望月薪</span>
				<span class="flexEnd color6 fs13">5k-6k<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>期望城市</span>
				<span class="flexEnd color6 fs13">西安<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>期望区域</span>
				<span class="flexEnd color6 fs13">高新区<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>当前状态</span>
				<span class="flexEnd color6 fs13">积极找工作<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			<div class="item pdtb15 flexRowBetween bordB1">
				<span>到岗时间</span>
				<span class="flexEnd color6 fs13">随时<img class="arrowR" src="../../static/images/arrow-icon.png" ></span>
			</div>
			
		</div>
		
		<div class="submitbtn" style="margin-top: 80px;">
			<button class="btn" type="button">保存</button>
		</div>
		
		<div class="black-bj" v-show="is_show"></div>
		<div class="seltShow radius8 whiteBj" v-show="is_seltShow">
			<div class="RcolseBtn" @click="seltShow">×</div>
			<p class="tt">全职</p>
			<p class="tt">兼职</p>
			<p class="tt">实习</p>
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
				is_seltShow:false
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			seltShow(){
				const self = this;
				self.is_show = !self.is_show;
				self.is_seltShow = !self.is_seltShow;
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
	@import "../../assets/style/editInfor.css";

</style>

