<template>
  <div class="bg-secondary p-2" style="height:100vh" >
    <ToDo />
  </div>
</template>

<script>
// @ is an alias to /src
import ToDo from "@/components/ToDo.vue";

export default {
  name: "Home",
  components: {
    ToDo,
  },
};
</script>
