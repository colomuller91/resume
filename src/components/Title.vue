<template>
  <div class="text-center py-3">
    <div class="flex justify-center items-center">
      <HorizontalLine class="flex-grow"/>
      <div>
        <p :class="big ? 'text-2xl font-bold px-2' : 'text-xl px-5' " class="uppercase">
          <slot></slot>
        </p>
      </div>
      <HorizontalLine class="flex-grow"/>
    </div>
  </div>

</template>

<script>
import HorizontalLine from "@/components/HorizontalLine";
export default {
  components:{
    HorizontalLine
  },
  props:{
    big:{
      default:false,
      type:Boolean
    }
  },
  name: "Title"
}
</script>

<style scoped>
  .text-center{
    text-align: center;
  }
</style>
