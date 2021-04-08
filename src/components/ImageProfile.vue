<template>
    <img
        class="rounded-full mx-auto mb-5 p-3"
        :src="require('../assets/imageprofile.jpeg')"
        alt="image-profile" />
</template>

<script>
export default {
name: "ImageProfile"
}
</script>

<style scoped>
  img{
    max-height: 250px;
    border: 3px solid black;
  }

</style>
