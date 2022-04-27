<template>
<div>
  <div class="ct-section ct-w80A">
      <h1>Since 2000, weve been partenering with education leaders tos <span> increase equiti and achievement</span> for all students</h1>
      <div class="card-section">
        <CardComponent v-for='card in about' :key='card.title' :title='card.title' :descr='card.descr' :imagine="card.imagine" />
       
      </div>

      <!-- Statistic Part -->
       <div class="statistics-section ct-w100a">
            <div class="ct-w30">
                <span class="ct-orange-shape ct-stat-bg green-text">6500</span> <span class="orange-text">+</span> <span>Students</span>
            </div>
            <div class="ct-w30">
                <span class="ct-red-shape ct-stat-bg orange-text">200</span> <span class="red-text">+</span> <span>Online Courses</span>
            </div>
            <div class="ct-w30">
                <span class="ct-green-shape ct-stat-bg green-text">6500</span> <span class="green-text">%</span> <span>Happy Clients</span>
            </div>
        </div>
    </div>

    <!-- Course -->
    <div class="ct-section ct-w80A">
        <h1>Recent Courses</h1>
        <p>Whether you're considering a foundation course or an undergraduate degree master's or PhD, accademics is a place where students thrive.</p>
        <div class="card-section">
            <CardComponent v-for='course in courses' :key='course.title' :imagine='course.imagine' :title='course.title' :descr='course.descr' />
        </div>
    </div>
</div>
</template>

<script>
import CardComponent from'@/components/CardComponent.vue';
import courses from '@/assets/data/courses.json';
import about from '@/assets/data/about.json';
export default {
 data(){
    return{
      about,
      courses,
    }
  },
  components:{
      CardComponent,
      
  },
  
}
</script>

<style lang='scss' scoped>
@import '@/assets/style/common.scss';
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

.orange-text{
    color:$orange-text;
}
.red-text{
    color:$red-text;
}
.green-text{
    color:$green-text;
}



</style>