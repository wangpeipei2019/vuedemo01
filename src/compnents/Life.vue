<template>
	
		<div id="life">
			<h3>生命周期函数的演示---{{msg}}</h3>
			<button @click="run()">执行方法</button>烦烦烦方法
		</div>
		
	
</template>

<script>
	export default {
		data() {
			return {
			msg:"生命周期函数"
			};
		}, methods:{
			run(){
				this.msg="改变后的值"
			}
		},
		beforeCreate() {
		console.info("实例刚刚被创建")	//
		},
		created() {
			console.info("实例已经创建完")
			//
		},
		beforeMount() {
			console.info("模板编译之前")
			//
		},
		mounted() {
			console.info("模板编译完")
			//
		},
		beforeUpdate() {
			console.info("数据更新之前")
			//
		},
		updated() {
			console.info("数据更新完毕")
		
		},
		beforeDestroy() {
			console.info("数据销毁前")
			//
		},destroyed() {
			console.info("数据销毁完成")
			//
		}
	}
</script>

<style>

</style>
