<template>
	<the-header title="Remember Me"></the-header>
	<stored-resources :resources="storedResources"></stored-resources>
</template>

<script>
	import StoredResources from './components/learning-resources/StoredResource.vue';
	import TheHeader from  './components/layouts/TheHeader.vue'

	export default{
		components:{
			StoredResources,
			TheHeader
		},

		data(){
			return{
				storedResources:[
					{
						id:'official-guide',
						title:'Official Guide',
						description: 'The official guide of VueJs',
						link:'https://vuejs.org'
					},
					{
						id:'vue-router',
						title:'Vue router',
						description: 'getting started with vue router',
						link:'https://vuejs.org/vue-router'
					},
				]
			}
		}
	};

</script>

<style>
	
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}

</style>