<template>
	<base-card>
		<base-button @click="setSelectedTab('stored-resources')">Stored Resources</base-button>
		<base-button @click="setSelectedTab('add-resource')">Add Resource</base-button>

		<component :is="selectedTab" />
	</base-card>
</template>

<script>
	import StoredResources from './StoredResource.vue';
	import AddResource from './AddResource.vue';

	export default{
		components:{
			StoredResources,
			AddResource,
		},
		data(){
			return {
				selectedTab: 'stored-resources',
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
			
		},
		provide(){
			return{
				resources: this.storedResources
			};
		},
		methods: {
			setSelectedTab(tab){
				this.selectedTab = tab
			}
		},

	};
</script>

<style>
	

</style>