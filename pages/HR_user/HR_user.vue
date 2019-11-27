<template>
	<div>
		
		<div class="userHead flexRowBetween whiteBj">
			<h1 class="ll fs20 ftw">张三伞</h1>
			<div class="flexEnd">
				<img class="Rphoto" src="../../static/images/workbench-img1.png"/>
			</div>
		</div>
		
		<div class="userdata pdtb10">
			<ul class="flexRowBetween">
				<li class="item flexColumn">
					<h3 class="num">10</h3>
					<p class="text">总邀请</p>
				</li>
				<li class="item flexColumn">
					<h3 class="num">6</h3>
					<p class="text">已面试</p>
				</li>
				<li class="item flexColumn">
					<h3 class="num">4</h3>
					<p class="text">待面试</p>
				</li>
			</ul>
		</div>
		
		<div class="XlineNav whiteBj">
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/HR_userInfor/HR_userInfor'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon1.png">
					<span class="tt">HR信息</span>
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
			<div class="info flexRowBetween" @click="Router.navigateTo({route:{path:'/pages/HR_user_dataStats/HR_user_dataStats'}})">
				<div class="flex">
					<img class="icon" src="../../static/images/about-icon4.png">
					<span class="tt">数据统计</span>
				</div>
				<div class="right flexEnd">
					<img class="arrowR" src="../../static/images/arrow-icon.png" >
				</div>
			</div>
			<div class="f5H10"></div>
			<div class="info center" @click="Router.navigateTo({route:{path:'/pages/user/user'}})">切换至公司账户</div>
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
			
			<div class="navbar_item"  @click="Router.navigateTo({route:{path:'/pages/HR_user/HR_user'}})">
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
				is_show:false
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
	.userHead{padding: 20px 4%;}
	.userHead .ll{ width: 80%;}
	.userHead .Rphoto{width: 60px; height: 60px;border-radius: 50%;display: block;}
	
	.userdata{background: #eaf3ff;}
	.userdata .item{width: 33.3%;position: relative;}
	.userdata .item .num{font-size: 18px;color: #398EF9; margin-bottom: 5px;}
	.userdata .item .text{font-size: 12px; color: #666;}
	.userdata .item:after{content: ''; width: 0px; height: 25px;border-right: 1px dashed #398EF9;position: absolute;right: 0;top: 50%;transform: translateY(-50%);}
	.userdata .item:last-child:after{display: none;}
	
	.XlineNav .info{padding: 15px 4%;border-bottom: 1px solid #eee;}
	.XlineNav .icon{width: 15px;height: 15px;margin-right: 10px; display: block;}

</style>

