<template>
  <div class='ct-w100 ct-h80px '>
      <div class="ct-w80A ct-h80px ct-header">
          <div class="ct-w10">
              <img src="../assets/img/Logo.jpg"  alt="">
          </div>
          <div class="ct-header-list">
              <a href="">Home</a>
              <a href="">About</a>
              <a href="">Academics</a>
              <a href="">Courses</a>
              <a href="">News</a>
          </div>

      </div>
      

  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
@import '../assets/style/common.scss';
.ct-header{
    display:flex;
    justify-content:space-between;

    .ct-header-list{
        display: flex;
        align-items:center;

        a{
            margin-left:15px;
            font-weight: bold;
            
            &:hover{
                color:#d74d52;
            }
        }
    }
}

img{
    width:90%;
}



</style>