<template>
  <div class=" ct-video-section">
      <div class="ct-video">
          <div class='ct-play'>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 213.7 213.7"><circle class="circle" fill="white" cx="106.8" cy="106.8" r="103.3"/><path class="triangle" fill="#D74D52" d="M73.5 62.5l75 43.3-75 43.3z"/></svg>
          </div>
         

      </div>
      <div class="ct-upcoming-section">
          <div class="ct-w50 upcoming-title">
              <h1>Upcoming Events</h1>
          </div>
          <div class="upcoming-desc">
              <p>Princeton offers admission information sessions and student-led tours to campus visitors</p>
              <button>Learn more <span><i class="fa-solid fa-angle-right"></i></span> </button>
              <p>Admission information sessions and student-led tours to campus visitors</p>
              <button>Learn more  <span><i class="fa-solid fa-angle-right"></i></span></button>
          </div>
          <button class='upcoming-locations'> <span><i class="fa-regular fa-map"></i>  </span> Event Locations  <span><i class="fa-solid fa-angle-right"></i></span></button>

      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
@import '@/assets/style/common.scss';
.ct-video-section{
    aspect-ratio: 1.8;
    width:100%;
    position:relative;
}
.ct-video{
    top:0;
    left:0;
    background-image: url('@/assets/img/video-bg-3.jpg');
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    overflow: hidden;
    z-index:0;
    justify-content: center;
    align-items:center;

    &:hover{
        z-index:2;
    }
    .ct-play{
        width:20%;
        cursor:pointer;
    }
}

.ct-upcoming-section{
    right:0;
    bottom:0;
    z-index:1;
    flex-direction: column;
    background-color: #ffffff;

    .upcoming-desc{
        width:75%;
        padding:20px 10px 20px 20px;

        p{
           font-size:1.4rem;
           margin:1.2em 0;
       }
       button{
           border:none;
           background:none;

            &:hover{
            background-color:rgba(0, 0, 0, 0.1);
        }
       }
      

    }
     .upcoming-locations{
           width:20%;
           border:none;
           align-self: center;
           margin-top:2em;
           background:none;

            &:hover{
            background-color:rgba(0, 0, 0, 0.1);
        }

       }
    

    

    .upcoming-title{
        align-self:center;
     }

    h1{
        padding:30px;
        background-color:$red1-background;
        color:white;
    }
   
    
}

.ct-video,
.ct-upcoming-section{
    position:absolute;
    width:60%;
    aspect-ratio:1.3;
    box-shadow: 5px 5px 15px 3px rgba(119, 119, 119, 0.2);
    display: flex;
}


</style>