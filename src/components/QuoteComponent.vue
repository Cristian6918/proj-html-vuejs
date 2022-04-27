<template>
  <div class='ct-w80A quote-section'>
      <h1>"Accademic was committed to my success from the moment I attended an Open House. Withe the support of caring <span class='red-underline'>advisors, professors, and staff</span>  i was able the thrive in courses, gain recognition through scholarship, and finish <strong>with confidence in my <a href="#" class='red-underline'>@academic</a> abilities.</strong> "</h1>

  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
@import '@/assets/style/common.scss';

.red-underline{
    color:$red-text;
    text-decoration:underline;
    text-decoration-color:$red-text;
    
}
.quote-section{
    text-align: center;
   margin-top:3em !important;
   background-image: url('@/assets/img/quote.png');
   background-size: contain;
   background-repeat: no-repeat;
   background-position: center;

}


</style>