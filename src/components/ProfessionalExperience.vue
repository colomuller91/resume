<template>
  <div>
    <div
        class="mb-3"
        v-for="job in experience">
      <p class="text-lg">
        <span class="font-bold">{{job.title}}</span> - {{job.company}} <span class="ml-3 text-sm italic">[ {{job.from}} - {{job.to}} ]</span>
      </p>
      <p class="text-sm text-gray-700 ml-3">
        {{job.jobDescription}}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfessionalExperience",
  props:{
    experience:{
      required:true,
      type:Array
    }
  }
}
</script>

<style scoped>
*{
  text-align: left;
}

</style>
