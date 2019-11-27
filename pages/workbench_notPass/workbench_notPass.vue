<template>
	<div>
		
		<div class="pdlr4">
			<div class="bordB1 dafenList pdt15 fs12">
				<ul>
					<li class="item flexRowBetween pdb15">
						<div class="ll flex">
							<span class="tt color6 mgr10">沟通能力</span>
							<span class="fen"><em class="num one" style="width: 80%;"></em></span>
						</div>
						<div class="rr flexEnd color9">
							<input class="input" type="number" name="" id="" value="" />
							<span>分</span>
						</div>
					</li>
					<li class="item flexRowBetween pdb15">
						<div class="ll flex">
							<span class="tt color6 mgr10">逻辑能力</span>
							<span class="fen"><em class="num two" style="width: 60%;"></em></span>
						</div>
						<div class="rr flexEnd color9">
							<input class="input" type="number" name="" id="" value="" />
							<span>分</span>
						</div>
					</li>
					<li class="item flexRowBetween pdb15">
						<div class="ll flex">
							<span class="tt color6 mgr10">表达能力</span>
							<span class="fen"><em class="num three" style="width: 70%;"></em></span>
						</div>
						<div class="rr flexEnd color9">
							<input class="input" type="number" name="" id="" value="" />
							<span>分</span>
						</div>
					</li>
				</ul>
			</div>
			
			<div class="fs13 pdtb15">不合格原因</div>
			<div class="pingjia flex center fs13">
				<span class="btn" :class="{on:item.bOn}" @click="checkbox(index)" v-for="(item,index) in fuliData">{{item.title}}</span>
			</div>
			
			<div class="fs13 pdtb15">评价</div>
			<div>
				<textarea rows="" cols="" placeholder="请写出你对他的评价" value=""></textarea>
			</div>
		</div>
		
		<div class="goutong center flexRowBetween mgt40 pdt20 color6">
			<span class="item">不推荐</span>
			<span class="item on">推荐</span>
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
				fuliData:[
					{title:'不合适',bOn:true},
					{title:'没经验',bOn:false},
					{title:'学生',bOn:true},
					{title:'学历不符',bOn:false},
					{title:'没经验',bOn:false},
					{title:'经验少',bOn:false},
				]
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
	@import "../../assets/style/dafen.css";
	
</style>

