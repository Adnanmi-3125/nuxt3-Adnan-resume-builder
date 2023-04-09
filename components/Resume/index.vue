<template lang="">
    <div class="flex h-full flex-col justify-between">
      <div>      
      <div :style="{textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" v-show="items[0].checked" class="bg-gray-100 p-2 rounded-md">
        <UserProfile :selected="selected"/>
        <div class="border-b border-gray-300 ">
          <h4 :style="{fontSize:'12px', textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="text-sm text-gray-600 font-medium mt-1">Personal info</h4>
        </div>
        <div :style="{JustifyContent:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="flex items-center gap-2">
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Name</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Email</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Phone Number</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Address</h6>
         
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 ">Photo</h6>
        </div>
      </div>
      <div v-show="items[1].checked" class="mt-5">
        <div class="border-b border-gray-300 ">
          <h4 :style="{fontSize:'12px', textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="text-sm text-gray-600 font-medium mt-1">Skills</h4>
        </div>
        <div :style="{JustifyContent:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="flex items-center gap-2">
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Skill</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 ">Education</h6>
         
        </div>
      </div>
      <!-- Education section -->
      <div v-show="items[2].checked" class="mt-5">
        <div class="border-b border-gray-300 ">
          <h4 :style="{fontSize:'12px', textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="text-sm text-gray-600 font-medium mt-1">Education</h4>
        </div>
        <div :style="{JustifyContent:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="flex items-center gap-2">
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">School/Institute</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Field of Study</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Degree</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Summary</h6>
         
        </div>
      </div>
      <!-- Work Exprerience -->
      <div v-show="items[3].checked"  class="mt-5">
        <div class="border-b border-gray-300 ">
          <h4 :style="{fontSize:'12px', textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="text-sm text-gray-600 font-medium mt-1">Work Experience</h4>
        </div>
        <div :style="{JustifyContent:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="flex items-center gap-2">
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Company Name</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Location</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Designation</h6>
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2 border-r border-gray-400">Duration</h6>
         
        </div>
      </div>
      <!-- Career Objective -->
      <div v-show="items[4].checked" class="mt-5">
        <div class="border-b border-gray-300 ">
          <h4 :style="{fontSize:'12px', textAlign:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="text-sm text-gray-600 font-medium mt-1">Career Objective</h4>
        </div>
        <div :style="{JustifyContent:selected === 'center' ? 'center' : selected === 'right' ? 'right' : 'left'}" class="flex items-center gap-2">
          <h6 :style="{fontSize:'10px'}" class="text-xs text-gray-600 font-normal mt-1 pr-2">A short summary to outline your proffetional goals</h6>
         
         
        </div>
      </div>  
    </div> 
    <div class="flex mt-4 flex-col md:flex-row items-center gap-4 justify-between">
      <div class="flex gap-4 items-center">
       <img class="w-5 h-5 " src="~/assets/facebook.png"/>
       <img class="w-5 h-5 " src="~/assets/twitter.png"/>
       <img class="w-5 h-5 " src="~/assets/linkedin.png"/>
       <img class="w-5 h-5 " src="~/assets/share.png"/>
      
      </div>
      <div>
        <Buttons :background="'dark'" :title="'Download'"/>  
      </div>
  


    </div>
    </div>
</template>
<script>


export default {
  props: {
    items: {
      type: Array,
      required: true,
    },
    showModal:{
      type:Boolean,
      required:true
    },
    selected: {
      type: String,
      required: true,
    },
  },
 
  
};

</script>
<style lang="">
    
</style>