<template>
	<div>
		
		<!-- 推荐指数 -->
		<div class="pdlr4 mgtb20">
			<div class="flexRowBetween">
				<h1 class="fs15">推荐指数</h1>
				<p class="fs12 color9 flexEnd" @click="Router.navigateTo({route:{path:'/pages/resume_zhishu/resume_zhishu'}})">查看历史<img class="arrowR" src="../../static/images/arrow-icon.png" ></p>
			</div>
			<div class="dafenList pdt15 fs12">
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
		
		<div class="pdlr4 mgtb20 fabuzheInfor fs13">
			<h1 class="fs15">基础信息</h1>
			<div class="flexRowBetween pdt15 pdb5">
				<div class="half flexCenter"><img style="width: 75px;height: 90px;" src="../../static/images/resume-img.png" ></div>
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

