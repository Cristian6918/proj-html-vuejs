<template>
  <div id="app">
    <HeaderComponent />
    <HeroComponent />
    <MainComponent/>
    
    
  </div>
</template>

<script>

// import of Components
import HeaderComponent from '@/components/HeaderComponent.vue';
import HeroComponent from'@/components/HeroComponent.vue';
import MainComponent from '@/components/MainComponent.vue';


// import Json Files


export default {
  name: 'App',
 
  components: {
    HeaderComponent,
    HeroComponent,
    MainComponent
    
  },
  
 
}
</script>

<style lang="scss" >
@import '@/assets/style/common.scss';



</style>
