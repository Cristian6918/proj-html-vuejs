<template>
  <div class="ct-card">
      <img :src='imagine' :alt="imagine">
      <h4>{{title}}</h4>
      <p>{{descr}}</p>
     


  </div>
</template>

<script>
export default {
    props:['imagine','title','descr','price', 'by','id'],
}
</script>

<style lang='scss' scoped>




</style>