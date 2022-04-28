<template>
<div class='ct-w80A'>
  <div class="ct-section ">
      <h1>Since 2000, weve been partenering with education leaders tos <span> increase equiti and achievement</span> for all students</h1>
      <div class="card-section">
        <CardComponent v-for='card in about' 
        :key='card.title' 
        :title='card.title' 
        :descr='card.descr' 
        :imagine="card.imagine" 
        :personalizedClass="aboutClass"/>
      </div>

      <!-- Statistic Part -->
       <div class="statistics-section ct-w100a">
            <div class="ct-w30">
                <span class="ct-orange-shape ct-stat-bg orange-text">6500</span> 
                <span class="orange-text">+</span> 
                <span>Students</span>
            </div>
            <div class="ct-w30">
                <span class="ct-red-shape ct-stat-bg orange-text">200</span> 
                <span class="red-text">+</span> 
                <span>Online Courses</span>
            </div>
            <div class="ct-w30">
                <span class="ct-green-shape ct-stat-bg green-text">100</span> 
                <span class="green-text">%</span> 
                <span>Happy Clients</span>
            </div>
        </div>
    </div>

    <!-- Course -->
    <div class="ct-section">
        <div class="ct-w50">
        <h1>Recent Courses</h1>
        <p>Whether you're considering a foundation course or an undergraduate degree master's or PhD, accademics is a place where students thrive.</p>
        </div>
        <div class="card-section">
            <CardComponent v-for='course in courses' 
            :key='course.title' 
            :imagine='course.imagine' 
            :title='course.title' 
            :descr='course.descr' 
            :price="course.price" 
            :personalizedClass='coursesClass'/>
        </div>
    </div>
    <QuoteComponent />
    <VideoSectionComponent />
    <div class="ct-section">
        <div class="ct-w50">
            <h1>Latest from our Blogs</h1>
            <p>Whether you're considering a foundation course or an undergraduate degree master's or PhD, accademics is a place where students thrive.</p>
        </div>
        <div class="card-section">
            <CardComponent v-for='element in news' 
            :key='element.title' 
            :imagine='element.imagine' 
            :title='element.title' 
            :purpose="element.purpose[0]"
            :secondPurpose="element.purpose[1]"
            :personalizedClass='newsClass'/>
        </div>
    </div>
</div>
</template>

<script>
// import Components
import CardComponent from'@/components/CardComponent.vue';
import QuoteComponent from '@/components/QuoteComponent.vue';
import VideoSectionComponent from '@/components/VideoSectionComponent.vue';

// import Data
import courses from '@/assets/data/courses.json';
import about from '@/assets/data/about.json';
import news from '@/assets/data/news.json';
export default {
 data(){
    return{
      about,
      courses,
      news,
      aboutClass:'ct-about',
      coursesClass:'ct-course',
      newsClass:'ct-news'
    }
  },
  components:{
      CardComponent,
      QuoteComponent,
      VideoSectionComponent
      
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