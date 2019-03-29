<template>
	<div id="RouterA">A路由 
	 <ul>
        <li v-for="(item,key) in list">
             <router-link :to="'/ContentB/'+key">{{key}}--{{item}}</router-link>
        </li>
     </ul>

	
	</div>
	

</template>

<script>
	export default {
		data() {
			return {
				 msg:'我是一个新闻组件',    
               list:['111111','222222','333333']        

			};
		}
	}
</script>

<style>

</style>
