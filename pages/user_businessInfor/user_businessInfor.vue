<template>
	<div>
		
		<div class="pdlr4 mgtb15">
			<h1 class="fs15 ftw">基础信息</h1>
			<div class="editLine fs13">
				<ul>
					<li class="flex pdt10">
						<span class="title">公司名称：</span>
						<div class="rr">
							<input type="text" name="" value="" placeholder="请输入公司名称" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">联系人：</span>
						<div class="rr">
							<input type="text" name="" value="" placeholder="请输入联系人" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">手机号：</span>
						<div class="rr">
							<input type="number" maxlength="11" name="" value="" placeholder="请输手机号" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">座机号：</span>
						<div class="rr">
							<input type="number" name="" value="" placeholder="请输入座机号" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">邮箱：</span>
						<div class="rr">
							<input type="text" name="" value="" placeholder="请输入邮箱" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">公司规模：</span>
						<div class="rr">
							<input type="text" name="" value="" placeholder="请输入公司规模" />
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">公司地址：</span>
						<div class="rr">
							<input type="text" name="" value="" placeholder="请输入公司地址" />
						</div>
					</li>
				</ul>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="pdlr4 mgtb15">
			<h1 class="fs15 pdb10 ftw">公司简介</h1>
			<div>
				<textarea class="f5bj" rows="" cols="" placeholder="请输入公司简介"></textarea>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="pdlr4 mgtb15">
			<h1 class="fs15 pdb10 ftw">营业执照</h1>
			<div>
				<div class="rr upload_pic flex">
					<div class="item pr">
						<input class="upload" type="file" name="" value="" />
						<img class="pic" src="../../static/images/merchants-icon.png" >
					</div>
				</div>
			</div>
		</div>
		<div class="f5H10"></div>
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
	@import "../../assets/style/editInput.css";
	

</style>

