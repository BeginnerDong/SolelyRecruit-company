<template>
	<div>
		
		<div class="pdlr4 mgtb15">
			<h1 class="fs15 ftw">基础信息</h1>
			<div class="editLine fs13">
				<ul>
					<li class="flex pdt10">
						<span class="title">招聘职位：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="会计助理" placeholder="请输入招聘职位" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">工作年限：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="1年以上" placeholder="请输入工作年限" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">工资薪酬：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="1000-1500" placeholder="请输入工资薪酬" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">学历要求：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="大专以上" placeholder="请输入学历要求" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">年龄要求：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="20岁以上" placeholder="请输入年龄要求" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">性别要求：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="不限" placeholder="请输入性别要求" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">招聘人数：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="1" placeholder="请输入招聘人数" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
					<li class="flex pdt10">
						<span class="title">工作地点：</span>
						<div class="rr flexRowBetween">
							<div class="L-input">
								<input type="text" name="" value="陕西省西安市雁塔区高新大都荟" placeholder="请输入工作地点" />
							</div>
							<div class="Rarrow flexEnd">
								<img class="arrowR" src="../../static/images/arrow-icon.png" >
							</div>
						</div>
					</li>
				</ul>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="pdlr4 mgtb15">
			<h1 class="fs15 pdb10 ftw">职位要求</h1>
			<div>
				<textarea rows="" cols="" placeholder="请输入该职位的要求" value="职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求职位要求"></textarea>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="pdlr4 mgt15">
			<h1 class="fs15 pdb10 ftw">福利待遇</h1>
			<div class="pingjia flex center fs13">
				<span class="btn" :class="{on:item.bOn}" @click="checkbox(index)" v-for="(item,index) in fuliData">{{item.title}}</span>
			</div>
		</div>
		<div class="f5H10"></div>
		
		<div class="pdlr4 submitbtn mgt30">
			<button class="btn" type="button">发布</button>
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
					{title:'五险一金',bOn:true},
					{title:'包吃',bOn:false},
					{title:'包住',bOn:false},
					{title:'周末双休',bOn:false},
					{title:'年底双薪',bOn:true},
					{title:'房补',bOn:false},
					{title:'话补',bOn:false},
					{title:'交通补助',bOn:false},
					{title:'饭补',bOn:false},
					{title:'加班补助',bOn:true}
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
	@import "../../assets/style/editInput.css";
	@import "../../assets/style/dafen.css";
	
	
</style>

