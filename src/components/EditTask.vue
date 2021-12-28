<template>
  <section
    v-if="bools"
    class="bg-white h-100 w-100 position-absolute"
    style="z-index: 20"
    @click="closeModal"
  ></section>
  <section
    v-if="bools"
    class="position-absolute d-flex justify-content-center align-items-start p-2"
    style="
      z-index: 50;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      height: 100vh;
      margin-top: 20vh;
    "
  >
    <form
      class="mt-10 d-flex flex-column border border-dark p-2 border-3 h-50 position-fixed"
      @submit.prevent="editTask"
    >
      <input
        class="border rounded p-2 mb-2"
        v-model.lazy="newTask.title"
        placeholder="Title"
        type="text"
      />
      <textarea
        ref="texsearch"
        rows="20"
        class="border rounded p-2 mb-2"
        v-model.lazy="newTask.description"
        placeholder="Task Details"
        type="text"
      ></textarea>
      <button
        class="border rounded p-2 bg-success text-white"
        type="submit"
        @submit.prevent=""
      >
        New Task
      </button>
    </form>
  </section>
  <button @click="test">dd</button>
</template>

<script>
export default {
  inheritAttrs: false,
  name: "EditTask",
  props: ["tasker", "showVal", "bool"],
  data() {
    return {
      showVals: this.showVal,
      bools: this.bool,
      newTask: {
        title: "",
        description: "",
      },
    };
  },
  methods: {
    test() {
      console.log(this.bools);
      console.log(this.showVal);
    },
    ModalOpen() {
      this.bools = true;
    },
    closeModal() {
      this.bools = false;
    },
    showModal() {
      this.bools = true;
      // auto focus
      this.$nextTick(() => {
        this.$refs.textsearch.focus();
      });
    },
    showtheVal() {
      console.log(this.showtheVal);
    },
  },
};
</script>

<style></style>
