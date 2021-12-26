<template>

  <div class="dropdown">
    <button
      class="btn btn-secondary dropdown-toggle h-75"
      type="button"
      id="dropdownMenuButton1"
      data-bs-toggle="dropdown"
      aria-expanded="false"
    >
      {{ value }}
    </button>
    <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1" role="menu">
      <li v-for="option in options" :key="option">
        <a
          class="dropdown-item"
          @click="value = option"
          href="javascript:void(0)"
          >{{ option }}</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Dropdown",
  data() {
    return {
      options: ["Edit", "Delete"],
      value: "",
    };
  },
};
</script>


<style>
</style>