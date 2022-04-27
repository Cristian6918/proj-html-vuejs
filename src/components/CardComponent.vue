<template>
  <div :class="personalizedClass">
      <div class="ct-card-image">
        <img :src='imagine' :alt="imagine">
      </div>
      <div class="ct-card-descr">
        <p class='price-bg' >{{price}}</p>
        <h4>{{title}}</h4>
        <p>{{descr}}</p>
      </div>
     


  </div>
</template>

<script>
export default {
    props:['imagine','title','descr','price', 'by','id','personalizedClass'],
}
</script>

<style lang='scss' scoped>







</style>