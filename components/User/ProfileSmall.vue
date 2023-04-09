<template lang="">
  <div
    :style="{
      justifyContent:
        childProp === 'center'
          ? 'center'
          : childProp === 'left'
          ? 'left'
          : 'right',
    }"
    class="flex"
  >
    <div
      class="flex items-center justify-center relative w-6 h-6 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600"
    >
      <svg
        class="absolute w-6 h-6 mt-1 text-gray-400"
        fill="currentColor"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
          clip-rule="evenodd"
        ></path>
      </svg>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    childProp: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang=""></style>
