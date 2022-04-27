<template>
  <div :class="personalizedClass + ' ' +'ct-card'">
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
@import '@/assets/style/common.scss';

.ct-card{
    width:30%;
    display: flex;
    flex-direction: column;
    margin-top:3em;
    border-radius:10px;
    gap:2em;
    
    box-shadow: 5px 5px 15px 3px rgba(119, 119, 119, 0.2);

}

.ct-course{
    text-align:left;
    justify-content: space-between;
    img {
        height:100%;
        width:100%;
        object-fit: cover;
        
        &:hover{
             transform: scale(1.2);

        }
    }
}

.ct-about{
    justify-content: space-around;

    img {
        margin-top:2em;
        width: 25%;
        object-fit: contain;
        
    }
}



.ct-card-image {
    height: 50%;
    overflow: hidden;
    img{
        transition: transform 2s ease;
        
    }
}


.ct-card-descr {
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.price-bg {
    width:10%;
    background: $red-background;
    background: linear-gradient(180deg,  rgba(255, 255, 255, 0) 50%, $red-background , $red-background 10%);
}

.ct-card:hover{
    box-shadow: 5px 5px 15px 3px rgba(119, 119, 119, 0.4);;
}







</style>