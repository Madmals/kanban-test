<template >
  <button style="height: 5vh; z-index:60;" class="m-2" @click="ModalOpen">CreateTask</button>
  <section v-if="isModal" class="bg-white h-100 w-100 position-absolute" style="z-index:20;" @click="closeModal">

  </section>
  <section v-if="isModal" class="position-absolute d-flex justify-content-center align-items-start p-2" style="z-index:50;left:50%;top:50%;transform:translate(-50%,-50%);height:100vh;margin-top:20vh;">
    <form class=" mt-10 d-flex flex-column border border-dark p-2 border-3 h-50 position-fixed" @submit.prevent="addTask">
      <input
        class="border rounded p-2 mb-2"
        v-model.lazy="newTask.title"
        placeholder="Title"
        type="text"
      />
      <textarea rows="20"
        class="border rounded p-2 mb-2"
        v-model.lazy="newTask.description"
        placeholder="Task Details"
        type="text"
      />
      <button class="border rounded p-2 bg-success text-white" type="submit">New Task</button>
    </form>

  </section>


</template>

<script>
export default {
  name: "CreateTask",
  data() {
    return {

      isModal: false,
      newTask:{
	      title:"",
	      description:""
      }

    };
  },
  methods: {
	  ModalOpen(){
		  this.isModal = true;

	  },
	  closeModal(){
		  this.isModal = false;
	  }
  }
};
</script>

<style>
</style>