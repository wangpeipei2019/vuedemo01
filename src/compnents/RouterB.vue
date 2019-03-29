<template>
	<div>B路由
	<ul>
		<li v-for="(item,key) in list">
			<router-link :to="'/ContentA?id='+key">{{key}}--{{item}}</router-link>
		</li>
	</ul>
	  <button @click="goNews()">通过js跳转到新闻页面</button>

	</div>
	
	

</template>

<script>
	export default {
		data() {
			return {
				 msg:'我是一个组件',
               list:['商品111111','商品222222','商品333333']    
			};
		},
		methods:{
			 goNews(){

                //第一种跳转方式

                // this.$router.push({ path: 'RouterA' })


                 this.$router.push({ path: '/RouterA/495' });


                //另一种跳转方式

                    //在main.js里面加   { path: '/RouterA', component: News,name:'RouterA' },


                    // router.push({ name: 'RouterA', params: { userId: 123 }}) 动态路由


                  //  this.$router.push({ name: 'RouterA'})
            }

		}
	}
</script>

<style>

</style>
