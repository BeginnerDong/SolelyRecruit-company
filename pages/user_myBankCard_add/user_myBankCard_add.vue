<template>
	<div>
		
		<div class="userInfor pdlr4 fs13">
			<ul>
				<li>
					<span class="ll">银行卡开户名</span>
					<div class="rr"><input type="text" value="" placeholder="请输入银行卡开户名"></div>
				</li>
				<li>
					<span class="ll">选择银行卡</span>
					<div class="rr">
						<select>
							<option value ="请选择">请选择</option>
							<option value ="">中国银行</option>
							<option value ="">建设银行</option>
							<option value ="">工商银行</option>
						</select>
					</div>
				</li>
				<li>
					<span class="ll">银行卡卡号</span>
					<div class="rr"><input type="number" value="" placeholder="请输入银行卡卡号"></div>
				</li>
				<li>
					<span class="ll">手机号</span>
					<div class="rr"><input  type="number" value="" placeholder="请输入联系电话" onkeyup="this.value=this.value.replace(/\D/g,'')"  maxlength="11"></div>
				</li>
				<li>
					<span class="ll">验证码</span>
					<div class="rr flexEnd">
						<div style="width:50%;"><input type="number" value="" placeholder="请输入验证码"></div>
						<div class="yamTest pubColor pdl20">获取验证码</div>
					</div>
				</li>
			</ul>
		</div>
		
		<div class="submitbtn" style="margin-top: 100px;">
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
	
	.recharge ul{flex-wrap: wrap;}	
	.recharge .item{width: 47%; padding: 12px 10px; box-sizing: border-box; font-size: 13px; color: #666;border: 1px solid #eee;margin-bottom: 20px;border-radius: 8px;}
	.recharge .item .mny{font-size: 15px; color: #da251c;margin-bottom: 5px; font-weight: bold;}
	.recharge .item.on{background: #ebf4ff;border-color: #398EF9;}
	
</style>

