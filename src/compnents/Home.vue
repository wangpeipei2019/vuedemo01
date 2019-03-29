<template>
	
		<div id="home">
			<h1>父子组件传值：1.动态绑定属性。2.在子组件props接收父组件的数据</h1>
			<h2 >首页组件----{{msg}}</h2>
			<button @click="run()">执行方法</button>
			<v-head :title="title" :run="run" :home='this' ref='head'></v-head>
			
			<br />
			<h5>父主动获取子的数据方法：
			子组件定义一个ref="header";   在父组件里  this.$refs.header 属性//方法
			主动获取父组件的方法数据   this.$parent.msg/title .run()方法
			</h5>
			<button @click="childData()">主动获取子组件的方法</button>
			<v-news></v-news>
			
			
			
		</div>
	
</template>

<script>
	import Header from "../compnents/Header";
	import News from "../compnents/News";

	export default {
		data() {
			return {
			msg:"这是首页组件",
			title:"父子传值",
			
			};
		}, methods:{
			run(data){
				alert(this.msg+data)
			},
			childData(){
			//	alert(this.$refs.head.childData) 获取子组件的数据
			 this.$refs.head.runChild()
			}
		},
		components:{
			'v-head':Header,
			'v-news':News,
		}
	}
</script>

<style lag="scss" >
 
 #home{
	 h2{
	 color: red
	 } 
 }
	 
</style>
