<template>
	<div>
		
		<div class="loginCont">
			<h1 class="fs22 pdb20 ftw">账户密码登录</h1>
			<div class="item bordB1">
				<input type="text" value="" placeholder="请输入账号">
			</div>
			<div class="item bordB1">
				<input type="text" value="" placeholder="请输入密码">
			</div>
			
			<div class="submitbtn" style="margin-top: 80px;">
				<button type="button" class="Wbtn" @click="Router.navigateTo({route:{path:'/pages/index/index'}})">登录</button>
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
	@import "../../assets/style/login.css";

</style>

