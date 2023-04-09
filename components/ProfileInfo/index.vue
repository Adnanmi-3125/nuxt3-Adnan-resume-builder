<template lang="">
  <div>
    <div class="border-b py-3">
      <h4 class="text-sm font-medium ml-2">Personal info</h4>
    </div>
    <div class="py-4 flex items-center">
      <UserProfileIcon />
      <h6 class="text-sm font-normal ml-2">Profile photo</h6>
    </div>
    <div>
      <TextField label="Name" name="name" type="text" placeholder="John Doe" />
      <TextField
        label="Email"
        name="email"
        type="email"
        placeholder="name@company.com"
        required
      />
      <TextField
        label="Number"
        name="number"
        type="number"
        placeholder="1234567890"
      />
      <TextField
        label="Address"
        name="address"
        type="address"
        placeholder="123 Main St"
      />
    </div>
    <div>
        <Preview/>
    </div>
    <div>
        <ResumeLayout :selected="selected" @updateSelected="updateSelected"/>
    </div>
    <div class="pt-10 flex gap-3 items-center justify-between">
        <Buttons :background="'light'" :title="'Cancel'"/>
        <Buttons :background="'dark'" :title="'Save'"/>
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
      console.log("@@@@@@@@", event);
      this.$emit('update-layout', event);
    },
  },
};
</script>
<style lang=""></style>
