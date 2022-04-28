<template>
  <div>
      <!-- footer Hero -->
      <div class="footer-hero ct-w100">
          <div class='footer-hero-image'><img src="@/assets/img/gallery-3-3.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/news-3-2.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/gallery-1-3.jpg" alt=""></div>
          <div class='footer-hero-image'><img src="@/assets/img/gallery-2-3.jpg" alt=""></div>
      </div>


      <!-- Footer -->
      <div class="ct-footer-main">
          <div class="banner-part-footer ct-w80A">    
              <div class="search-part">
                 <input type="text" class='search-bar' placeholder="Subscribe to our Newsletter">
                  <div class="search-button">
                      <span>Subscribe</span>
                  </div>

              </div>
              <div class="search-part-info">
                  <p><a href="#">Insigths is Pickwik</a> Universtity's thought leadership publication for sharing knowledge oon management, tecnology and innovation</p>
                  <button >Learn more  <span><i class="fa-solid fa-angle-right"></i></span></button>

              </div>
              

          </div>
          <div class="footer-list-section ct-w80A">

          
            
            <FooterListComponent v-for='contact in contacts' 
                 :key='contact.id'
                 :title="contact.title"
                 :adress='contact.adress'
                 :tel='contact.tel'
                 :mail='contact.mail' />
       


            <FooterListComponent v-for='list in footerList' 
                :key='list.id'
                :title='list.title'
                :elements='list.elements'
                />
          </div>

      </div>
      <div class="footer-bottom ct-w100">
          <div class="ct-w80A footer-bottom-container">
              <div class="copyright">
                  <span>Copyright 2020 tophive. All Rights Reserved</span>
              </div>
              <div class="coockies">
                  <span>Privacy</span>
                  <span>Term</span>
                  <span>Cookie Policy</span>
                  <span>Sitemap</span>
              </div>

          </div>

      </div>

  </div>
</template>

<script>
import contacts from '@/assets/data/contact.json';
import footerList from '@/assets/data/FooterList.json';
import FooterListComponent from '@/components/FooterListComponent.vue';
export default {
    data(){
        return{
            contacts,
            footerList
        }
    },
    components:{
        FooterListComponent
    }


}
</script>

<style lang='scss' scoped>

@import '../assets/style/common.scss';


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


// footer

.ct-footer-main{
    background-color:$darkBlue-background ;
    padding-top:10vh;

   
    
}

 .banner-part-footer{
        display:flex;
        padding:3vh 100px;
        border-left: 10px solid #cccccc;
        box-shadow: 5px 5px 15px 3px rgb(25, 39, 53,0.9);


        
        

        

        .search-part{
            display:flex;
            width:50%;
            text-align:center;
            input{
                text-align:center;
            }
            

            .search-bar{
                width:60%;
                height:4vh;
                background-color:white;
                border:none;
                outline:none;
            }
            .search-button{
                width:20%;
                height:4vh;
                background-color: red;
                color:white;
                display: flex;
                align-items: center;
                justify-content: center;
                cursor:pointer;
            }

        }
        .search-part-info{
            width:50%;
            p{
                color:#cccccc;
            }
            a{
                color:$red-text;
                text-decoration: underline;
                text-decoration-color:#ffffffff;
            }
            button{
                border:none;
                outline:none;
                background: none;
                color:#cccccc;
                margin-top:10px;

                  &:hover{
                    color:#eeeeee;
                    }
            }
        }
        
        
    }

.footer-list-section{
        display:flex;
        margin-top:4em;
        justify-content: space-between;
        padding-bottom:3em;
    }

    .footer-bottom{
        background-color:#333333;
        padding:20px 0;
        color:#cccccc;
     
       

        .footer-bottom-container{
            display:flex;
            justify-content:space-between
        }
    }
    .copyright{
        width:40%;
    }
    .coockies{
        width:40%;
        display:flex;
        justify-content: space-between;
    }



</style>