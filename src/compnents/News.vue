<template>
	<div>
		<h1>非父子组件传值Header值--{{msg}}</h1>
		<h3> 1.新建一个js文件，引入vue,实例化Vue，暴露实例 2.在要广播的地方引入定义的实例
		 
		 3.通过VueEmit.$emit('名称','数据')；4.在接收数据的地方通过$on接收广播的数据
		 
		 VueEmit.$emit('名称',function(){
			 
		 })</h3>
		 
	</div>
</template>

<script>
	import VueEvent from"../model/VueEvent.js";
	export default {
		data() {
			return {
				msg:"er"
			};
		},
		mounted(){
			VueEvent.$on("to-news",function(a){
				console.log(a)
				
			})
		}
	}
</script>

<style>

</style>
