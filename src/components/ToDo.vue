<template>
  <section class="h-75 border border-success border-3 w-25">
    <h3 class="w-100 bg-secondary mb-2 rounded fs-4 p-2 text-white">To Do</h3>
    <Tasks :tasker="tasker" />
  </section>
</template>

<script>
import Tasks from "@/components/Tasks.vue";

export default {
  components: {
    Tasks,
  },
  name: "ToDo",
  props: ["tasker"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
