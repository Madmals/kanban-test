<template>
  <h1 class="w-25 bg-white rounded">To Do</h1>
  <section class="h-75 border w-25">
    <Tasks/>

  </section>
</template>

<script>
import Tasks from "@/components/Tasks.vue"


export default {
  components:{
    Tasks,
  },
  name: "ToDo",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
