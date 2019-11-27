<template>
	<div>
		
		<div class="positionList pdlr4 jobGuanli">
			<ul>
				<li class="flexRowBetween" v-for="item in positionDate">
					<div class="L_cont flexRowBetween pdtb15">
						<div class="flex ll">
							<img class="Lphoto" src="../../static/images/position-img.png" >
							<div class="infor">
								<p class="name fs14">会计助理</p>
								<p class="lable fs13">纯粹科技</p>
								<p class="color9 fs12">西安&nbsp;|&nbsp;1-3年&nbsp;|&nbsp;大专</p>
							</div>
						</div>
						<div class="rr">
							<div class="red mgb20 flexEnd">4K-6K</div>
							<p class="fs12 color9 flexEnd">10月20日</p>
						</div>
					</div>
					<div class="R_eidtBtn flexColumn fs10 center">
						<span class="item color6" @click="Router.navigateTo({route:{path:'/pages/user_jobGuanli_edit/user_jobGuanli_edit'}})">修改</span>
						<span class="item on" @click="deltAlert">删除</span>
					</div>
				</li>
			</ul>
		</div>
		
		<div class="xieyiAlert" v-if="is_show">
			<div class="infor center radius8 pdtb40 ">
				<div class="RcolseBtn"  @click="deltAlert">×</div>
				<div class="tit font16 mgb30">确认要删除这个职位吗？</div>
				<div class="btnB flexRowBetween">
					<div class="item">是</div>
					<div class="item on"  @click="deltAlert">否</div>
				</div>
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
				positionDate:[{},{},{}]
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			deltAlert(){
				const self = this;
				self.is_show=!self.is_show;
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
	@import "../../assets/style/workbench.css";
	
	.jobGuanli ul li{border-bottom: 1px solid #eee;}
	.jobGuanli li .ll img.Lphoto{width: 60px;height: 60px;}
	.jobGuanli .L_cont{width: 85%;}
	.jobGuanli .R_eidtBtn{width: 15%; align-items: flex-end;}
	.jobGuanli .R_eidtBtn .item{width: 30px;height: 30px;background: #f5f5f5;line-height: 30px;}
	.jobGuanli .R_eidtBtn .item.on{background: #398EF9;color: #fff;}
	
	.xieyiAlert{background: rgba(0,0,0,0.5);position: fixed;top: 0;right: 0;bottom: 0;left: 0; z-index: 999;}
	.xieyiAlert .infor{width: 80%; min-height: 100px;position: fixed; top: 50%;left:50%;transform: translate(-50%,-50%);background: #fff; box-sizing: border-box;z-index: 1000;color: #555;}	
	.btnB{ width: 60%;margin: 0 auto;}
	.btnB .item{width:50px; line-height: 25px; height: 25px;border-radius: 20px;border:1px solid #ddd;}
	.btnB .item.on{background: #398EF9; border-color: #398EF9;color: #fff;}
</style>

