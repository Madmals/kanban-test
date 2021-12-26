<template>
  <h3 class="w-25 bg-secondary mb-2 rounded fs-4 p-2 text-white">To Do</h3>
  <section class="h-75 border border-success border-3 w-25">
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
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
