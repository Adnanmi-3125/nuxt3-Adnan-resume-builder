<template lang="">
    <div>
       <Toggle :items="items" @toggle="handleChildClick"/> 
    </div>
</template>
<script>
export default {
    props: {
    items: {
      type: Array,
      required: true,
    }
  },
  methods: {
    handleChildClick(index) {
        this.$emit('toggle-checked',index);
    },
  },
}
</script>
<style lang="">
    
</style>