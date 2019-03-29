<template>
	
		<div>
			<h2>头部组件（传值篇）--{{title}}</h2>
			<button @click="run(123)">执行父组件的方法</button>
			<button @click="runParent()">获取父组件的数据和方法</button>
			<button @click="getParent()">主动获取父组件的数据和方法</button>
			<button @click="toEvent()">非父子传值给News</button>
		</div>
	
</template>

<script>
	import VueEvent from"../model/VueEvent.js";
	
	export default {
		data() {
			return {
				Hmsg:"headerData",
				childData:"child"
			};
			
		},
		methods:{
			runParent(){
				alert(this.title) //this.home.title
			},
			runChild(){
				alert("获取了子组件方法")
			},
			getParent(){
				alert(this.$parent.msg)
			},
			toEvent(){
				VueEvent.$emit("to-news",this.Hmsg)
			}
				
		},
		
		
		props:['title','run'],
	}
</script>

<style>

</style>
