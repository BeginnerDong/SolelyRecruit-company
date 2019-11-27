<template>
	<div>
		
		<div class="userHead flexRowBetween whiteBj">
			<div class="ll">
				<h1 class="fs20 mgb10">纯粹科技</h1>
				<p class="fs12 flex color6" @click="Router.navigateTo({route:{path:'/pages/user_businessInfor/user_businessInfor'}})">编辑公司信息</p>
			</div>
			<div class="flexEnd">
				<img class="Rphoto" src="../../static/images/workbench-img1.png"/>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="XlineNav whiteBj">
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_myAssets/user_myAssets'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon.png">
					<span class="tt">我的资产</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div  class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_businessInfor/user_businessInfor'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon1.png">
					<span class="tt">公司信息</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_fabuRecruit/user_fabuRecruit'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon2.png">
					<span class="tt">发布招聘</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_jobGuanli/user_jobGuanli'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon3.png">
					<span class="tt">职位管理</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_dataStats/user_dataStats'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon4.png">
					<span class="tt">数据统计</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/user_HRGuanli/user_HRGuanli'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon5.png">
					<span class="tt">HR管理</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="f5H10"></div>
			<div class="info pdtb15 flexCenter" @click="Router.navigateTo({route:{path:'/pages/login_HR/login_HR'}})">切换至我是HR</div>
		</div>
		
		<!--底部tab键-->
		<div class="navbar flexRowBetween">
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/index/index'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar1.png" />
				</div>
				<div class="text">搜人才</div>
			</div>
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/workbench/workbench'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar2.png" />
				</div>
				<div class="text">工作台</div>
			</div>
			
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/user/user'}})">
				<div class="nav_img">
					<img src="../../static/images/nabar3-a.png" />
				</div>
				<div class="text this-text">个人中心</div>
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
	@import "../../assets/style/navbar.css";
	
	page{background: #F5F5F5;}
	.userHead{padding: 25px 4%;}
	.userHead .ll{ width: 80%;}
	.userHead .Rphoto{width: 60px; height: 60px;border-radius: 50%;display: block;}
	
	.XlineNav .info{padding: 15px 4%;border-bottom: 1px solid #eee;}
	.XlineNav .icon{width: 15px;height: 15px;margin-right: 10px; display: block;}

</style>

