<template>
  <Task class="mt-2" :task="tasker" />
</template>

<script>
import Task from "@/components/Task.vue"
export default {
	name:'Tasks',
	components:{
		Task,
	},
	data(){
		return{
		tasker:{
			title:'Siram Pokok',
			description: 'Siram pokok hari-hari pokok pon sihat'
		},

		}
	}

}
</script>

<style>

</style>