<template>
  <div
    v-for="(item, index) in tasker"
    :items="item"
    :key="index"
    class="border border-dark border-3 p-2 m-2 rounded-3"
  >
    <section class="d-flex justify-content-between">
      <h4 class="w-50 font-weight-bold fs-5">
        <u>{{ item.title }}</u>
      </h4>
      <Dropdown
        @edit-task="showval"
        @edit-task-index="show(item, index)"
        @delete-task="del(index)"
        :index="index"
      />
    </section>
    <p class="text-start m-2">{{ item.description }}</p>
    <EditTask
      :showVal="showVal"
      :bool="bool"
      @set-bool="setBool"
      @run-test="test"
    />
  </div>
</template>

<script>
import Dropdown from "@/components/Dropdown.vue";
import EditTask from "@/components/EditTask.vue";

export default {
  inheritAttrs: false,
  components: {
    Dropdown,
    EditTask,
  },
  data() {
    return {
      bool: false,
      editTask: "aaa",
      taks: {
        items: "",
        index: "",
      },
      showVal: "",
    };
  },
  name: "Task",
  props: ["tasker"],
  methods: {
    setBool(value) {
      this.bool = value;
    },
    show(item, index) {
      this.taks.items = item;
      this.taks.index = index;
    },
    showval(val) {
      if (val == "Edit") {
        setTimeout(() => {
          this.showVal = this.taks;
        }, 1000);
        this.bool = !this.bool;
      }
    },
  },

};
</script>

<style></style>
