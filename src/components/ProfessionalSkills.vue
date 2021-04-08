<template>
  <div>
    <div
        class="mb-1"
        v-for="(skill, skillName) in skills">
      <p>
        {{skillName}}
        <span v-if="skill.skill_level" class="ml-2">
          <span v-for="i in score_base" class="mx-0.5">
            <font-awesome-icon
                class="mb-0.5"
                :style="{color: i <= skill.skill_level ? 'rgb(134 232 134)' : '#CCC', fontSize:'10px'}"
                icon="circle"/>
          </span>
        </span>
      </p>
      <p class="text-xs italic ml-3">[ {{ skill.frameworks.join(', ') }} ]</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfessionalSkills",
  props:{
    skills:{
      required:true,
      type:Object
    },
    score_base:{
      type:Number,
      default: 5
    }
  }
}
</script>

<style scoped>
 *{
   text-align: left;
 }

</style>
