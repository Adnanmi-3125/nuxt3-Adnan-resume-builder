<template>
  <div class="flex justify-center items-center h-screen relative">
    <button
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      @click="showModal = true"
    >
      Create your Resume
    </button>

    <div
      v-if="showModal"
      class="fixed top-0 left-0 w-full h-full flex items-start justify-center bg-black bg-opacity-50 overflow-auto"
    >
      <div
        class="bg-white rounded-lg shadow-lg overflow-hidden relative w-90 h-90"
      >
        <div class="px-4 py-2 flex justify-between items-center">
          <div class="flex items-center">
            <button
              class="text-gray-500 hover:text-gray-600"
              @click="showModal = false"
            >
              <svg
                class="h-3 w-3"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M10 19l-7-7m0 0l7-7m-7 7h18"
                />
              </svg>
            </button>
            <h2 class="text-lg font-medium ml-2">Resume Builder</h2>
          </div>
          <button
            class="text-gray-500 hover:text-gray-600"
            @click="showModal = false"
          >
            <svg
              class="h-4 w-4"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div class="p-4">
          <div
            class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 it h-full"
          >
            <div
              class="border flex flex-col lg:col-span-1 md:col-span-1 border-gray-400 col-span-2 justify-between rounded-lg p-4"
            >
              <Settings @toggle-checked="toggleChecked" :items="items" />
              <div class="pt-10 flex gap-3 flex-col items-end justify-end">
                <Buttons :background="'light'" :title="'Add Custome Section'" />
                <div class="border-b w-full border-gray-400" />
                <Buttons :background="'dark'" :title="'Import Resume'" />
                <Buttons :background="'light'" :title="'Change Template'" />
              </div>
            </div>
            <div class="border border-gray-400 col-span-2 rounded-lg p-4 pb-0">
              <Resume
                :selected="selected"
                :items="items"
              />
            </div>
            <div
              class="border border-gray-400 lg:col-span-1 md:col-span-1 col-span-2 rounded-lg px-4"
            >
              <ProfileInfo :selected="selected" @update-layout="updateLayout" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: "",
      showModal: false,
      items: [
        { label: "Personal Info", checked: true },
        { label: "Skills", checked: true },
        { label: "Education", checked: true },
        { label: "Work Experience", checked: true },
        { label: "Carrier Objective", checked: true },
      ],
    };
  },

  methods: {
    toggleChecked(index) {
      this.items[index].checked = !this.items[index].checked;
    },
    updateLayout(selected) {
      this.selected = selected;
    },
  },
};
</script>

<style>
.w-90 {
  width: 90%;
  margin-top: 100px;
  margin-bottom: 50px;
}
</style>
