<template>
<section class="d-flex flex-column bg-">

  <div class="p-2 d-flex justify-content-between" style="height:100vh" >
    <ToDo />
    <CreateTask class="border rounder "  />
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
};
</script>
