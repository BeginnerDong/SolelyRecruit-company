<template>
	<div>
		
		<div class="pdlr4">
			<div class=" mgtb20 recharge">
				<ul class="flexRowBetween">
					<li class="item flexColumn" :class="curr==index?'on':''" @click="changeCurr(index)" v-for="(item,index) in amountDate" :key="index">
						<h1 class="mny">300元</h1>
						<p>到账：310元</p>
					</li>
				</ul>
			</div>
			<div class="submitbtn" style="margin-top: 100px;">
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
				is_show:false,
				amountDate:[{},{},{},{}],
				curr:0
			}
		},
		onLoad() {
			const self = this;
			// self.$Utils.loadAll(['getMainData'], self);
		},
		methods: {
			changeCurr(index){
				const self = this;
				self.curr=index
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
	@import "../../assets/style/NavTab.css";
	
	.recharge ul{flex-wrap: wrap;}	
	.recharge .item{width: 47%; padding: 12px 10px; box-sizing: border-box; font-size: 13px; color: #666;border: 1px solid #eee;margin-bottom: 20px;border-radius: 8px;}
	.recharge .item .mny{font-size: 15px; color: #da251c;margin-bottom: 5px; font-weight: bold;}
	.recharge .item.on{background: #ebf4ff;border-color: #398EF9;}
	
</style>

