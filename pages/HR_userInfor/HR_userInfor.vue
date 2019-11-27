<template>
	<div>
		
		<div class="editLine pdlr4 fs13 ">
			<ul>
				<li class="flex pdtb15 bordB1">
					<span class="title">姓名：</span>
					<div class="rr">
						<input type="text" name="" value="" placeholder="请输入姓名" />
					</div>
				</li>
				<li class="flex pdtb15 bordB1">
					<span class="title">手机号：</span>
					<div class="rr">
						<input type="number" maxlength="11" name="" value="" placeholder="请输手机号" />
					</div>
				</li>
				<li class="flex pdtb15 bordB1">
					<span class="title">座机号：</span>
					<div class="rr">
						<input type="number" name="" value="" placeholder="请输入座机号" />
					</div>
				</li>
				<li class="flex pdtb15 bordB1">
					<span class="title">邮箱：</span>
					<div class="rr">
						<input type="text" name="" value="" placeholder="请输入邮箱" />
					</div>
				</li>
			</ul>
		</div>
		
		<div class="pdlr4 submitbtn mgt30">
			<button type="button" class="btn">确定</button>
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

