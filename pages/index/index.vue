<template>
	<div>
		
		<div class="flexRowBetween seachbox fs13">
			<div class="flex white"  @click="Router.navigateTo({route:{path:'/pages/index_jobEdit/index_jobEdit'}})">
				<img class="Licon mgr5" src="../../static/images/search-talent-icon.png" >
				<span>会计</span>
				<img class="arrowR" src="../../static/images/search-talent-icon1.png" >
			</div>
			<div class="flexRowBetween rr">
				<div class="input">
					<input type="" name="" id="" value="" placeholder="搜人才" />
				</div>
				<button class="seachBtn" type="button"></button>
			</div>
		</div>
		<div class="h60 pdt15"></div>
		<div class="positionList">
			<ul>
				<li class="pdlr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetailTwo/resumeDetailTwo'}})">
					<div class="flexRowBetween pdtb15">
						<div class="flex ll">
							<img class="Lphoto" src="../../static/images/search-talent-img.png" >
							<div class="infor">
								<p class="name fs14">会计助理</p>
								<p class="lable fs13">克莱</p>
								<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
							</div>
						</div>
						<div class="rr">
							<div class="red mgb20 flexEnd">4K-6K</div>
							<p class="fs12 color9 flexEnd">10月20日</p>
						</div>
					</div>
					<div class="pdtb15 flexEnd sourceBox fs12">
						<img class="pto" src="../../static/images/search-talent-img1.png" >
						<span class="mgl10 flex">杨飒<em class="mglr3">·</em>纯粹科技</span>
						<span class="color6 mgl5 mgr15">10-20</span>
						<span class="source hr">HR推荐</span>
					</div>
				</li>
				<li class="pdlr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetailTwo/resumeDetailTwo'}})">
					<div class="flexRowBetween pdtb15">
						<div class="flex ll">
							<img class="Lphoto" src="../../static/images/search-talent-img.png" >
							<div class="infor">
								<p class="name fs14">会计助理</p>
								<p class="lable fs13">克莱</p>
								<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
							</div>
						</div>
						<div class="rr">
							<div class="red mgb20 flexEnd">4K-6K</div>
							<p class="fs12 color9 flexEnd">10月20日</p>
						</div>
					</div>
					<div class="pdtb15 flexEnd sourceBox fs12">
						<img class="pto" src="../../static/images/search-talent-img1.png" >
						<span class="mgl10">杨飒</span>
						<span class="color6 mgl5 mgr15">10-20</span>
						<span class="source user">用户推荐</span>
					</div>
				</li>
				<li class="pdlr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetailTwo/resumeDetailTwo'}})">
					<div class="flexRowBetween pdtb15">
						<div class="flex ll">
							<img class="Lphoto" src="../../static/images/search-talent-img.png" >
							<div class="infor">
								<p class="name fs14">会计助理</p>
								<p class="lable fs13">克莱</p>
								<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
							</div>
						</div>
						<div class="rr">
							<div class="red mgb20 flexEnd">4K-6K</div>
							<p class="fs12 color9 flexEnd">10月20日</p>
						</div>
					</div>
					<div class="pdtb15 flexEnd sourceBox fs12">
						<span class="color6 mgl5 mgr15">10-20</span>
						<span class="source hr">系统推荐</span>
					</div>
				</li>
			</ul>
		</div>
		
		<!--底部tab键-->
		<div class="navbar flexRowBetween">
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/index/index'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar1-a.png" />
				</div>
				<div class="text this-text">搜人才</div>
			</div>
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/workbench/workbench'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar2.png" />
				</div>
				<div class="text">工作台</div>
			</div>
			
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/user/user'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar3.png" />
				</div>
				<div class="text">个人中心</div>
			</div>
		</div>
		<!--底部tab键 end-->
		
	</div>
</template>


<script>
	export default {
		data() {
			return {
				Router:this.$Router,
				showView: false,
				is_show:false,
				positionDate:[{},{},{},{},{}]
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			addContShow(){
				const self = this;
				self.is_show = !self.is_show
				self.is_addContShow = !self.is_addContShow
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
	@import "../../assets/style/navbar.css";
	@import "../../assets/style/workbench.css";	

</style>

