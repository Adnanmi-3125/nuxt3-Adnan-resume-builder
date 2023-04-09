<template lang="">
  <div class="w-full">
    <button
      type="button"
      :style="{
        backgroundColor: background === 'light' ? '#f0f4fa' : '#000000',
        color: background === 'light' ? '#000000' : '#ffffff',
      }"
      class="w-full py-1.5 px-5 mr-2 mb-2 text-xs font-medium text-gray-900 focus:outline-none bg-white rounded-full hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-1 focus:ring-gray-200 dark:focus:ring-gray-700 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700"
    >
      {{ title }}
    </button>
  </div>
</template>
<script>
export default {
  props: {
    background: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
  mounted() {
    this.logItems();
  },
  methods: {
    logItems() {
      console.log("items", this.background);
    },
  },
};
</script>
<style lang=""></style>
