<template>
<section class="d-flex flex-column bg-">

  <div class="p-2 d-flex justify-content-between" style="height:100vh" >
    <ToDo :tasker="tasker" />
    <CreateTask @new-task="addTasktoTasks" :tasker="tasker" class="border rounded"  />
  </div>

</section>
</template>

<script>
// @ is an alias to /src
import ToDo from "@/components/ToDo.vue";
import CreateTask from "@/components/CreateTask.vue";


export default {
  name: "Home",
  components: {
    ToDo,
    CreateTask,
  },
  	data(){
		return{
		tasker:[{
			title:'Siram Pokok',
			description: 'Siram pokok hari-hari pokok pon sihat'
		}],

		}
	},
  methods:{
    addTasktoTasks(value){
      this.tasker.push(value);
      console.log(value);
      console.log(this.tasker)
    }

  }
};
</script>
