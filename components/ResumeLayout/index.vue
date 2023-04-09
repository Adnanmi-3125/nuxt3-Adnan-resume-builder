<template lang="">
  <div class="">
    <!-- align to left layout -->
    <div class="border-b w-full border-gray-700 pb-3">
      <div class="flex items-end gap-2 mt-4">
        <input
          id="default-radio-1"
          type="radio"
          value="left"
          @input="updateSelected"
          name="default-radio"
          class="w-3 h-3 text-blue-600 bg-gray-100 border-gray-300 dark:ring-offset-gray-800 dark:bg-gray-700 dark:border-gray-600"
        />
        <div class="border-b w-full">
          <UserProfileSmall :childProp="'left'" />
          <h6 :style="{ fontSize: '12px' }" class="text-sm font-medium">
            Susan Singh
          </h6>
        </div>
      </div>
      <p
        :style="{ fontSize: '10px' }"
        class="text-gray-500 dark:text-gray-800 text-xs ml-5"
      >
        susan.smit.@gmail.com| +1956523586| Cambridge, MA 02139, United State
      </p>
    </div>
    <!-- align to center layout -->
    <div class="border-b w-full border-gray-700 pb-3">
      <div class="flex items-end gap-2 mt-4">
        <input
          @input="updateSelected"
          id="default-radio-1"
          type="radio"
          value="center"
          name="default-radio"
          class="w-3 h-3 text-blue-600 bg-gray-100 border-gray-300 dark:ring-offset-gray-800 dark:bg-gray-700 dark:border-gray-600"
        />
        <div class="border-b w-full text-center">
          <UserProfileSmall :childProp="'center'" />
          <h6 :style="{ fontSize: '12px' }" class="text-sm font-medium">
            Susan Singh
          </h6>
        </div>
      </div>
      <p
        :style="{ fontSize: '10px' }"
        class="text-gray-500 text-center dark:text-gray-800 text-xs ml-5"
      >
        susan.smit.@gmail.com| +1956523586| Cambridge, MA 02139, United State
      </p>
    </div>
    <!-- align to right layout -->
    <div>
      <div class="flex items-end gap-2 mt-4">
        <input
          @input="updateSelected"
          id="default-radio-1"
          type="radio"
          value="right"
          name="default-radio"
          class="w-3 h-3 text-blue-600 bg-gray-100 border-gray-300 dark:ring-offset-gray-800 dark:bg-gray-700 dark:border-gray-600"
        />
        <div class="border-b w-full text-end">
          <UserProfileSmall :childProp="'right'" />
          <h6 :style="{ fontSize: '12px' }" class="text-sm font-medium">
            Susan Singh
          </h6>
        </div>
      </div>
      <p
        :style="{ fontSize: '10px' }"
        class="text-gray-500 dark:text-gray-800 text-xs ml-5 text-end"
      >
        susan.smit.@gmail.com| +1956523586| Cambridge, MA 02139, United State
      </p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    selected: {
      type: String,
      required: true,
    },
  },
  methods: {
    updateSelected(event) {
      this.$emit("updateSelected", event.target.value);
    },
  },
};
</script>
<style lang=""></style>
