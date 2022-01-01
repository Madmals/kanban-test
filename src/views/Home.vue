<template>
  <section class="d-flex flex-column bg-">
    <div class="p-2 d-flex justify-content-between" style="height: 100vh">
      <ToDo :tasker="tasker" @edit-task-new="addTask" @test-focus="clear" />
      <CreateTask
        @new-task="addTasktoTasks"
        :tasker="tasker"
        class="border rounded"
        :isModal="modalOpen"
      />
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
  data() {
    return {
      focus:false,
      tasker: [
        {
          title: "Siram Pokok",
          description: "Siram pokok hari-hari pokok pon sihat",
        },
      ],
    };
  },
  methods: {
    addTasktoTasks(value) {
      this.tasker.push(value);
    },

    addTask() {
      this.emitter.on("edit-task-new", (val) => {
        console.log(val.newTask)
        this.tasker[val.index] =  val.newTask
      });
    },
    
  },
  mounted() {
    this.addTask();
  },
};
</script>
