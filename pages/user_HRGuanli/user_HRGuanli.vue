<template>
	<div>
		
		<div class="pdlr4 fs14">
			<ul>
				<li class="myBetween flexRowBetween pdtb15 bordB1" v-for="(item,index) in rechargNotes" :key="index">
					<span class="ll flex">
						<img class="photo" src="../../static/images/workbench-img1.png" >
						<span>张厉害</span>
					</span>
					<span class="rr flexEnd">15648985326</span>
				</li>
			</ul>
		</div>
		
		<div class="fix-addBtn" @click="Router.navigateTo({route:{path:'/pages/user_HRGuanli_add/user_HRGuanli_add'}})"><img src="../../static/images/mangement-icon.png"/></div>
		
	</div>
</template>


<script>
	export default {
		data() {
			return {
				Router:this.$Router,
				showView: false,
				is_show:false,
				rechargNotes:[{},{},{}]
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
	.myBetween .ll,.myBetween .rr{width: 50%;}
	.myBetween .ll .photo{width: 40px; height: 40px;border-radius: 50%;display: block; margin-right: 5px;}
	
	.fix-addBtn{border-radius: 50%; position: fixed; right: 4%;bottom: 40%; box-shadow: 0 0 5px rgba(0, 70, 158, 0.6); display: block;}
	.fix-addBtn img{width: 45px; height: 45px; display: block; margin: 0 auto;}
	
</style>

