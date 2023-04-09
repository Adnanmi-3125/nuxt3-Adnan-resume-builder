<template lang="">
  <div>
    <div class="border-b py-3">
      <h4 class="text-sm font-medium ml-2">Preview</h4>
    </div>
    <div>
      <div
        class="flex items-center rounded-lg p-2 mt-5 gap-2 border border-gray-400"
      >
        <img
          class="w-8 h-8 rounded-full"
          src="~/assets/user.webp"
          alt="s"
        />
        <div class="dark:text-white">
          <div
            :style="{ fontSize: '10px' }"
            class="text-gray-500 dark:text-gray-500"
          >
            Hey john how would you like to customize the personal info
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang=""></style>
