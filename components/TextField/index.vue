<template lang="">
  <div>
    <label :for="name" :style="{fontSize:'10px'}" class="block text-sm font-medium text-gray-900"
      >{{label}}</label
    >
    <input
    :style="{fontSize:'10px'}"
    :type="type" :name="name" :id="name" :placeholder="placeholder" :required="required" v-model="value" @input="$emit('input', $event.target.value)"
      class="border border-gray-300 text-gray-900 text-sm rounded-md focus:ring-blue-500 focus:border-blue-500 block w-full p-1.5"
      placeholder="name@company.com"
    />
  </div>
</template>
<script>
export default {
  props: {
    label: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    type: {
      type: String,
      required: true,
      validator: (value) => ['text', 'email', 'number', 'address'].includes(value)
    },
    placeholder: {
      type: String,
      required: false,
      default: ''
    },
    required: {
      type: Boolean,
      required: false,
      default: false
    }
  },
  data() {
    return {
      value: ''
    }
  }
}
</script>
<style lang=""></style>
