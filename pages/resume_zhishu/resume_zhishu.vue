<template>
	<div>
		
		<!-- 推荐指数 -->
		<div v-for="(item,index) in zhishuData" :key="index">
			<div class="pdlr4 mgtb20">
				<div class="dafenList fs12">
					<ul>
						<li class="item flexRowBetween pdb10">
							<div class="ll flex">
								<span class="tt color6 mgr10">沟通能力</span>
								<span class="fen"><em class="num one" style="width: 80%;"></em></span>
							</div>
							<div class="rr flexEnd color9">
								<span class="oneTex">8分</span>
							</div>
						</li>
						<li class="item flexRowBetween pdb10">
							<div class="ll flex">
								<span class="tt color6 mgr10">逻辑能力</span>
								<span class="fen"><em class="num two" style="width: 60%;"></em></span>
							</div>
							<div class="rr flexEnd color9">
								<span class="twoTex">6分</span>
							</div>
						</li>
						<li class="item flexRowBetween pdb10">
							<div class="ll flex">
								<span class="tt color6 mgr10">表达能力</span>
								<span class="fen"><em class="num three" style="width: 70%;"></em></span>
							</div>
							<div class="rr flexEnd color9">
								<span class="threeTex">7分</span>
							</div>
						</li>
					</ul>
				</div>
				<div class="flex fs12 ">
					<p>面试未通过原因：</p>
					<div class="ms-result flex color6" style="width: 70%;">
						<span class="span two">薪资不和</span>
						<span class="span three">薪资不和</span>
						<span class="span four">薪资不和</span>
					</div>
				</div>
				<div class="fs12 pdt10 pdb15">评语：<span class="color6">根据产品开发需求和变更，配合相关部门完成产品各部分的更新和修改</span></div>
				<div class="flexRowBetween">
					<div class="flex">
						<img class="mgr10" style="width: 40px;height: 40px;display: block;" src="../../static/images/resume-img2.png"/>
						<p>王建东<em class="dian">·</em>纯粹科技</p>
					</div>
					<div class="flexEnd pubColor fs13">面试：会计</div>
				</div>
			</div>
			<div class="f5H10"></div>
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
				zhishuData:[{},{},{}]
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
	@import "../../assets/style/workbench.css";
	@import "../../assets/style/dafen.css";
	
</style>

