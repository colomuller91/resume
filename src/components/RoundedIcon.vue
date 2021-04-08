<template>
  <div class="flex justify-center">
    <div :style="{backgroundColor:'#000', lineHeight:0}"
         class="p-4 rounded-full w-16 h-16 circle">
      <font-awesome-icon
          :style="{color:color, fontSize:'30px'}"
          :icon="icon"/>
    </div>
  </div>
</template>

<script>
export default {
  name: "RoundedIcon",
  props:{
    icon:{
      required:true,
      type:String
    },
    color:{
      default:'#FFF'
    }
  }
}
</script>

<style scoped lang="less">
  .circle{
    position: relative;
    &>*{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%,-50%);
    }
  }
</style>
