<template>
	<div>
		
		<div class="userInfor pdlr4 fs13">
			<ul>
				<li>
					<span class="ll">姓名</span>
					<div class="rr"><input type="text" value="" placeholder="请输入姓名"></div>
				</li>
				<li>
					<span class="ll">账号</span>
					<div class="rr"><input type="text" value="" placeholder="请输入账号"></div>
				</li>
				<li>
					<span class="ll">密码</span>
					<div class="rr"><input type="number" value="" placeholder="请输入密码"></div>
				</li>
			</ul>
		</div>
		
		<div class="submitbtn" style="margin-top: 120px;">
			<button class="btn">保存</button>
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
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			checkbox(i){
				const self = this;
				self.fuliData[i].bOn = !self.fuliData[i].bOn
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
	@import "../../assets/style/editInput.css";
	
	
</style>

