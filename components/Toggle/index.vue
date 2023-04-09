<template>
  <ul class="">
    <li
      v-for="(item, index) in items"
      :key="index"
      class="flex items-center justify-between border-b py-3"
    >
      <label class="relative inline-flex items-center mr-5 cursor-pointer">
        <input
          type="checkbox"
          class="sr-only peer"
          :checked="!checked"
          @change="toggleChecked(index)"
        />
        <div
          class="w-7 h-4 bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-black-300 dark:peer-focus:ring-black-800 dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-3 after:w-3 after:transition-all dark:border-gray-600 peer-checked:bg-black"
        ></div>
        <span class="ml-3 text-xs font-medium text-gray-900 dark:text-black">{{
          item.label
        }}</span>
      </label>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="20"
        height="20"
        viewBox="0 0 32 32"
      >
        <path
          fill="currentColor"
          d="m16 28l-7-7l1.41-1.41L16 25.17l5.59-5.58L23 21l-7 7zm0-24l7 7l-1.41 1.41L16 6.83l-5.59 5.58L9 11l7-7z"
        />
      </svg>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true,
    },
  },

  methods: {
    toggleChecked(index) {
      this.$emit("toggle", index);
    },
  },
};
</script>

<style>
/* Add any additional styles here */
</style>
