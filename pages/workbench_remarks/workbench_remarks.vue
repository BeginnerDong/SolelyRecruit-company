<template>
	<div>
		
		<div class="pdlr4 mgtb30">
			<div class="pdb10">备注</div>
			<div>
				<textarea style="height: 120px;" rows="" cols="" placeholder="写出你的备注信息"></textarea>
			</div>
			
			<div class="submitbtn" style="margin-top: 200px;">
				<button class="btn" type="button">确定</button>
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
</style>

