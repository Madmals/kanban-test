<template>
<div>
  <Task class="mt-2" :tasker="tasker" @send-delete="del"/>
</div>
</template>

<script>
import Task from "@/components/Task.vue"
export default {
	name:'Tasks',
	editTask:"",
	components:{
		Task,
	},
	props:['tasker'],


	



}
</script>

<style>

</style>