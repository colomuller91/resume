<template>
  <div>
    <div
        class="mb-3"
        v-for="project in projects">
      <p class="text-lg">
        <span class="font-bold">{{ project.title }}</span>
      </p>
      <p v-if="project.description" class="text-sm text-gray-700 ml-3 mb-4">
        {{ project.description }}
      </p>
      <ul class="link-list ml-4" v-if="project.linkList">
        <li v-html="link" v-for="link in project.linkList"></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  props: {
    projects: {
      required: true,
      type: Array
    }
  }
}
</script>

<style scoped>
* {
  text-align: left;
}
a{
  color: darkgreen;
}

</style>
