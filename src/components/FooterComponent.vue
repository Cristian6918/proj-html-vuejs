<template>
  <div>
      <div class="footer-hero ct-w100">
          <div class='footer-hero-image'><img src="@/assets/img/gallery-3-3.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/news-3-2.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/gallery-1-3.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/gallery-2-3.jpg" alt=""></div>
        
          
          
          

      </div>

  </div>
</template>

<script>
export default {


}
</script>

<style lang='scss' scoped>
.footer-hero{
    border-bottom:1px solid white;
    display: flex;
    margin-top:4em;

    .footer-hero-image{
        width:25%;
        overflow:hidden;
       
       

        img{
            height: 100%;;
            width:100%;
            object-fit: cover;
            transition: transform 2s ease;

            &:hover{
                transform: scale(1.1);
            }
        }
    }

}

</style>