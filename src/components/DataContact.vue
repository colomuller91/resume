<template>
  <div>
    <table>
      <tr v-for="(value,key) in data_contact" :key="key">
        <td width="40%" align="right">{{key}} :</td>
        <td width="60%" align="left">{{value}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "DataContact",
  props:{
    data_contact:{
      type:Object,
      required:true
    }
  }
}
</script>

<style scoped lang="less">

td{
  &:first-child{
    padding-right: 20px;
  }
}


</style>
