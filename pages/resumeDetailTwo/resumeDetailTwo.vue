<template>
	<div>
		
		<div class="pdlr4 mgtb20 fabuzheInfor fs13">
			<h1 class="fs15">基础信息</h1>
			<div class="flexRowBetween pdt15 pdb5">
				<div class="half flexCenter"><img style="width: 75px;height: 90px;" src="../../static/images/resume-img.png" /></div>
				<div class="half">
					<div class="flex">
						<h1 class="fs18">华路卓</h1>
						<span class="mgl15 mgt5">男&nbsp;&nbsp;未婚</span>
					</div>
					<div class="flex mgtb15">
						<img class="icon" src="../../static/images/resume-icon.png" >
						<span>152****5623</span>
					</div>
					<div class="flex">
						<img class="icon" src="../../static/images/resume-icon1.png" >
						<span>menggg****622</span>
					</div>
				</div>
			</div>
			<div class="flexRowBetween" style="flex-wrap: wrap;">
				<p class="half mgt10">出生年月：<em class="color6">2008.06.06</em></p>
				<p class="half mgt10">最高学历：<em class="color6">大专</em></p>
				<p class="half mgt10">工作经验：<em class="color6">无经验</em></p>
				<p class="half mgt10">目前状态：<em class="color6">已离职</em></p>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<!-- 教育经历 -->
		<div class="pdlr4">
			<h1 class="pdt15 fs15">教育经历</h1>
			<div class="positionList resumeList">
				<ul>
					<li class="pdtb15">
						<div class="flex ll">
							<img class="Lphoto" src="../../static/images/resume-icon2.png" >
							<div class="infor fs12">
								<h1 class="name fs15">陕西科技大学</h1>
								<p class="color6">本科/会计</p>
								<p class="color9 ">2014-2018</p>
							</div>
						</div>
					</li>
				</ul>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<!-- 工作经历 -->
		<div class="pdlr4">
			<h1 class="pdt15">工作经历</h1>
			<div class="positionList resumeList">
				<ul>
					<li class="pdtb15">
						<div class="flexRowBetween">
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/resume-icon3.png" >
								<div class="infor fs12">
									<h1 class="name fs15">APP设计</h1>
									<p class="color6">华路卓科技有限公司</p>
									<p class="color9 ">2018.10-2019.11</p>
								</div>
							</div>
						</div>
						<div class="fs13 pdb5 pdt10">工作内容</div>
						<div class="fs12 color6 xqInfor">
							<div class="cont">
								<p>1.负责移动APP和PC端软件界面的UE/UI设计，包括外观元素以及风格把控。</p>
								<p>2.负责在UE/UI设计中提现产品的视觉整体性。</p>
								<p>3.根据产品开发需求换和变更，配合相关部门完成产品个部分的更新和修改。</p>
							</div>
						</div>
					</li>
					<li class="pdtb15">
						<div class="flexRowBetween">
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/resume-icon3.png" >
								<div class="infor fs12">
									<h1 class="name fs15">APP设计</h1>
									<p class="color6">华路卓科技有限公司</p>
									<p class="color9 ">2018.10-2019.11</p>
								</div>
							</div>
						</div>
						<div class="fs13 pdb5 pdt10">工作内容</div>
						<div class="fs12 color6 xqInfor">
							<div class="cont">
								<p>1.负责移动APP和PC端软件界面的UE/UI设计，包括外观元素以及风格把控。</p>
								<p>2.负责在UE/UI设计中提现产品的视觉整体性。</p>
								<p>3.根据产品开发需求换和变更，配合相关部门完成产品个部分的更新和修改。</p>
							</div>
						</div>
					</li>
				</ul>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<!-- 图集 -->
		<div class="pdlr4">
			<h1 class="pdtb15">图集</h1>
			<div class="upImgbox flex bordB1">
				<div class="item pr">
					<img class="pic" src="../../static/images/resume-img1.png" >
				</div>
				<div class="item pr">
					<img class="pic" src="../../static/images/resume-img1.png" >
				</div>
				<div class="item pr">
					<img class="pic" src="../../static/images/resume-img1.png" >
				</div>
				<div class="item pr">
					<img class="pic" src="../../static/images/resume-img1.png" >
				</div>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="goutong center flexRowBetween pdt20 color6">
			<span class="item">不合适</span>
			<span class="item on">合适</span>
		</div>
		
		
	</div>
</template>


<script>
	export default {
		data() {
			return {
				Router:this.$Router,
				showView: false,
				is_show:false
			}
		},
		onLoad() {
			const self = this;
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
	@import "../../assets/style/xqInfor.css";
	@import "../../assets/style/dafen.css";
	@import "../../assets/style/resumeDetail.css";
	
	
</style>

