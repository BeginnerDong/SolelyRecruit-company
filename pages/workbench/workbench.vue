<template>
	<div>
		
		<div class="tooling_indNav f5bj color6">
			<div class="list flexRowBetween">
				<div class="item" :class="curr==1?'on':''" @click="change('1')">待邀约</div>
				<div class="item" :class="curr==2?'on':''" @click="change('2')">待面试</div>
				<div class="item" :class="curr==3?'on':''" @click="change('3')">已面试</div>
			</div>
		</div>
		
		<div v-show="curr==1">
			<div class="samllNav flex color6 fs13 bordB1">
				<span class="item" :class="num==1?'on':''" @click="chageSamll('1')">系统推荐</span>
				<span class="item" :class="num==2?'on':''" @click="chageSamll('2')">自主投递</span>
				<span class="item" :class="num==3?'on':''" @click="chageSamll('3')">邀约未确认</span>
				<span class="item" :class="num==4?'on':''" @click="chageSamll('4')">邀约拒绝</span>
			</div>
			
			<div class="positionList">
				<ul>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetail/resumeDetail'}})">
							<span class="fxIcon"><img src="../../static/images/workbench-icon.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb10 mglr4 fs12 inviter">
							<div class="flex">
								<img class="pt mgr10" src="../../static/images/workbench-img1.png" >
								<div class="">
									<p>张丹·纯粹科技</p>
									<p class="color9">10月20日</p>
								</div>
							</div>
							<div class="btnB flexEnd center color6">
								<span class="btn on" @click="inviteShow">确认邀请</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetail/resumeDetail'}})">
							<span class="fxIcon"><img src="../../static/images/workbench-icon1.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb10 mglr4 fs12 inviter">
							<div class="flex">
								<div class="">
									<p>张丹·纯粹科技</p>
									<p class="color9">10月20日</p>
								</div>
							</div>
							<div class="btnB flexEnd center color6">
								<span class="btn on" @click="inviteShow">确认邀请</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetail/resumeDetail'}})">
							<span class="fxIcon"><img src="../../static/images/workbench-icon2.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb10 mglr4 fs12 inviter">
							<div class="flex"></div>
							<div class="btnB flexEnd center color6">
								<span class="btn on"  @click="inviteShow">确认邀请</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetail/resumeDetail'}})">
							<span class="fxIcon"><img src="../../static/images/workbench-icon0.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb10 mglr4 fs12 inviter">
							<div class="flex"></div>
							<div class="btnB flexEnd center color6">
								<span class="btn on" @click="inviteShow">确认邀请</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4" @click="Router.navigateTo({route:{path:'/pages/resumeDetail/resumeDetail'}})">
							<span class="fxIcon"><img src="../../static/images/workbench-icon.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="pdlr4 flexEnd ing fs13 pdb10">等待用户确认</div>
					</li>
				</ul>
			</div>
		</div>
		
		<div v-show="curr==2">
			<div class="positionList">
				<ul>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4">
							<span class="fxIcon"><img src="../../static/images/workbench-icon.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb15 mglr4 fs12 inviter">
							<div class="flex">面试时间：2019.11.13</div>
							<div class="btnB flexEnd center color6">
								<span class="btn">关闭</span>
								<span class="btn on" @click="delayShow">延期</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4">
							<span class="fxIcon"><img src="../../static/images/workbench-icon1.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="flexRowBetween pdtb15 mglr4 fs12 inviter">
							<div class="flex">面试时间：2019.11.13</div>
							<div class="btnB flexEnd center color6">
								<span class="btn">关闭</span>
								<span class="btn on" @click="delayShow">延期</span>
							</div>
						</div>
					</li>
				</ul>
			</div>
		</div>
		
		<div v-show="curr==3">
			<div class="samllNav flex color6 fs13 bordB1">
				<span class="item" :class="numTwo==1?'on':''" @click="chageFinish('1')">已入职</span>
				<span class="item" :class="numTwo==2?'on':''" @click="chageFinish('2')">待入职</span>
			</div>
			
			<div class="positionList">
				<ul>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4">
							<span class="fxIcon"><img src="../../static/images/workbench-icon.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="pdtb10 mglr4 fs12 inviter">
							<div class="">备注：放假回公司来看和各说各话好几个会返利多少个供货方简单说两个号</div>
							<div class="btnB flexEnd center color6">
								<span class="btn on">未到岗</span>
							</div>
						</div>
					</li>
					<li>
						<div class="liwap flexRowBetween pdtb15 pr mglr4">
							<span class="fxIcon"><img src="../../static/images/workbench-icon1.png"/></span>
							<div class="flex ll">
								<img class="Lphoto" src="../../static/images/workbench-img.png" >
								<div class="infor">
									<p class="name fs14">张益达</p>
									<p class="lable fs13">会计</p>
									<p class="color9 fs12">西安&nbsp;|&nbsp;3年&nbsp;|&nbsp;本科</p>
								</div>
							</div>
							<div class="rr">
								<div class="red mgb20 flexEnd">4K-6K</div>
							</div>
						</div>
						<div class="pdtb10 mglr4 fs12 inviter flexRowBetween">
							<div class="">面试时间：201911.13</div>
							<div class="btnB flexEnd center color6">
								<a class="btn" href="workbench_notPass.html">不通过</a>
								<span class="btn on">入职</span>
							</div>
						</div>
						<div class="pdtb10 mglr4 fs12 inviter flexRowBetween">
							<div>备注：价格付款商量好苟富贵规划局分</div>
							<div class="mgl20 flexEnd" @click="Router.navigateTo({route:{path:'/pages/workbench_remarks/workbench_remarks'}})">
								<img class="addIcon" src="../../static/images/workbench-icon5.png" >
							</div>
						</div>
					</li>
					
				</ul>
			</div>
		</div>
		
		<div class="black-bj" v-show="is_show"></div>
		<!-- 选择邀约时间弹框 -->
		<div class="inviteShow whiteBj radius8" v-show="is_inviteShow">
			<div class="RcolseBtn"  @click="inviteShow">×</div>
			<p class="center">请选择时间</p>
			<div class="flexCenter mgtb20 setTime flexRowBetween">
				<div class="timeInput"><input type="datetime" name="" id="" value="" placeholder="请选择时间" /></div>
				<img class="timeIcon" src="../../static/images/workbench-icon4.png"/>
			</div>
			<div class="submitbtn">
				<button class="Wbtn" style="border-radius: 5px;" type="button">确定</button>
			</div>
		</div>
		
		<!-- 重新选择邀约时间弹框 -->
		<div class="inviteShow whiteBj radius8" v-show="is_delayShow">
			<div class="RcolseBtn"  @click="delayShow">×</div>
			<p class="center">请重新选择时间</p>
			<div class="flexCenter mgtb10 setTime flexRowBetween">
				<div class="timeInput"><input type="datetime" name="" id="" value="" placeholder="请选择时间" /></div>
				<img class="timeIcon" src="../../static/images/workbench-icon4.png"/>
			</div>
			<div class="mgb15">
				<textarea rows="" cols="" placeholder="请输入理由"></textarea>
			</div>
			<div class="submitbtn">
				<button class="Wbtn" style="border-radius: 5px;" type="button">确定</button>
			</div>
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
					<img src="../../static/images/nabar2-a.png" />
				</div>
				<div class="text this-text">工作台</div>
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
				curr:1,
				num:0,
				is_inviteShow:false,
				is_delayShow:false,
				numTwo:0
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			change(curr){
				const self = this;
				if(curr!=self.curr){
					self.curr = curr
				}
			},
			chageSamll(num){
				const self = this;
				if(num!=self.num){
					self.num = num
				}
			},
			chageFinish(numTwo){
				const self = this;
				if(numTwo!=self.numTwo){
					self.numTwo = numTwo
				}
			},
			inviteShow(){
				const self = this;
				self.is_show = !self.is_show
				self.is_inviteShow =!self.is_inviteShow
			},
			delayShow(){
				const self = this;
				self.is_show = !self.is_show
				self.is_delayShow =!self.is_delayShow
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
	@import "../../assets/style/NavTab.css";
	@import "../../assets/style/workbench.css";
	
	page{padding-bottom: 70px;}
	.positionList li .inviter{border-bottom: 0;}
	/* .setTime input{text-align: left;} */
	
</style>

