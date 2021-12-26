<template >
<div class="border border-dark border-3 p-2 m-2 rounded-3">
  <section class="d-flex justify-content-between">
    <h4 class="w-50 font-weight-bold fs-5"><u>{{ task.title }}</u></h4>
    <Dropdown/>
  </section>
  <p class="text-start m-2">{{task.description}}</p>
  </div>
</template>

<script>
import Dropdown from "@/components/Dropdown.vue"

export default {
components:{
	Dropdown,
},
  name: "Task",
  props: ["task"],
};
</script>

<style>
</style>