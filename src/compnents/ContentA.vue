<template>
	<div id="ContentA">详情页面A</div>
</template>

<script>
	export default {
		data() {
			return {
				mgs:"详情"
			};
		},
		mounted(){

              //获取get传值
				console.log(this.$route.query);
				
             
        }

	}
</script>

<style>

</style>
