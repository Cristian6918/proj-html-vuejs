<template>
  <div :class="personalizedClass + ' ' +'ct-card'">
      <div class="ct-card-image">
        <img :src='imagine' :alt="imagine">
      </div>
      <div class="ct-card-descr">
        <p class='price-bg' >{{price}}</p>
        <div class='ct-purpose'><span>
                <i v-if='purpose==="University"' class="fa-regular fa-folder-closed"></i>
                <i v-if='purpose==="Admin"' class="fa-regular fa-user"></i>  {{purpose}}
            </span>
            <span>
                <i v-if='secondPurpose==="University"' class="fa-regular fa-folder-closed"></i>
                <i v-if='secondPurpose==="Admin"' class="fa-regular fa-user"></i>  {{secondPurpose}}
            </span>
        </div>
        <h4>{{title}}</h4>
        <div class='ct-newsLine' v-if='personalizedClass==="ct-news"'></div>
        <button v-if='personalizedClass==="ct-news"'>Learn more  <span><i class="fa-solid fa-angle-right"></i></span></button>
        <p>{{descr}}</p>

      </div>
     


  </div>
</template>

<script>
export default {
    props:['imagine','title','descr','price', 'by','id','personalizedClass',"purpose",'secondPurpose','line'],
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
    button{
        max-width:30%;
        border:none;
        background:none;

        &:hover{
            background-color:rgba(0, 0, 0, 0.1);
        }
       }

}

.ct-course,
.ct-news{
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
    cursor:pointer;

}

.price-bg {
    width:10%;
    background: $red-background;
    background: linear-gradient(180deg,  rgba(255, 255, 255, 0) 50%, $red-background , $red-background 10%);
}

.ct-card:hover{
    box-shadow: 5px 5px 15px 3px rgba(119, 119, 119, 0.4);;
}

.ct-purpose{
    display:flex;
    gap:20px;
}

.ct-news:hover .ct-newsLine{
    width:100%;
    transition:width 2s;
}

.ct-newsLine{
    width:20%;
    height:2px;
    background-color:$red1-background;
}







</style>