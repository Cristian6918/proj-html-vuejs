<template>
  <div class='ct-w100 ct-h100h ct-hero'>
       <div class="ct-w80A ">
           <h1>Professional Devlopment For Coaches And Leaders</h1>
           <button>Learn More</button>

       </div>

  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
@import '../assets/style/common.scss';

.ct-hero{
   background-image: url('../assets/img/02_Landing-Page.jpg ');
   background-position: center;
   background-size:cover;
   display:flex;
   align-items: center;

   div{
       display: flex;
       align-items:center;
       justify-content: center;
       flex-direction: column;
       

       h1{  
           width:70%;
           font-weight: normal;
           font-size:4em;
           text-align:center;
       }

       button{
           padding:20px 40px;
           background-color:rgba(0, 0, 0, 0);
           outline: none;
           border:1px solid $border-button;
       }
   }


}

   

</style>