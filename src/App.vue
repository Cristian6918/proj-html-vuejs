<template>
  <div id="app">
    <HeaderComponent />
    <HeroComponent />
    <MainComponent/>
    <FooterComponent/>
    
    
  </div>
</template>

<script>

// import of Components
import HeaderComponent from '@/components/HeaderComponent.vue';
import HeroComponent from'@/components/HeroComponent.vue';
import MainComponent from '@/components/MainComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';


// import Json Files


export default {
  name: 'App',
 
  components: {
    HeaderComponent,
    HeroComponent,
    MainComponent,
    FooterComponent
    
  },
  
 
}
</script>

<style lang="scss" >
@import '@/assets/style/common.scss';



</style>
