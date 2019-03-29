<template>
	<div id="ContentB">详情页面B</div>
</template>

<script>
	export default {
		data() {
			return {
				mgs:"详情Parms"
			};
		},
		mounted(){

                /*获取动态路由传值*/
				console.log(this.$route.params);

        }
	}
</script>

<style>

</style>
