<template>
  <div class="ct-section ct-w80A">
      <h1>Since 2000, weve been partenering with education leaders tos <span> increase equiti and achievement</span> for all students</h1>
      <div class="card-section">
        <CardComponent v-for='card in about' :key='card.title' :title='card.title' :descr='card.descr' :imagine="getImage()" />
       
      </div>
       <div class="statistics-section ct-w100a">
            <div class="ct-w30">
                <span class="ct-orange-shape ct-stat-bg">6500</span> <span style="color:#f28202">+</span> <span>Students</span>
            </div>
            <div class="ct-w30">
                <span class="ct-red-shape ct-stat-bg">6500</span> <span style="color:#f28202">+</span> <span>Students</span>
            </div>
            <div class="ct-w30">
                <span class="ct-green-shape ct-stat-bg">6500</span> <span style="color:#f28202">+</span> <span>Students</span>
            </div>

        </div>

    </div>
</template>

<script>
import CardComponent from'@/components/CardComponent.vue';
import about from '@/assets/data/about.json';
export default {
 data(){
    return{
      about,
    }
  },
  components:{
      CardComponent,
      
  },
   methods:{
        getImage(){
          
            return require(`@/assets/svg/svg-0.svg`);
            
        }
    }
}
</script>

<style lang='scss' scoped>
.ct-stat-bg{
    background-size: contain;
    background-repeat: no-repeat;
}
.ct-orange-shape{
    background-image: url('@/assets/img/counter-shape-1-1-1.png ');
}
.ct-red-shape{
    background-image: url('@/assets/img/counter-shape-2-1-1.png ');
}
.ct-green-shape{
    background-image: url('@/assets/img/counter-shape-3-1-1.png ');
}

</style>