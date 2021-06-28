<template>
  <div id="main-content">
    <div class="container">
      <MainPromote></MainPromote>
      <CarouselProducts></CarouselProducts>
    </div>
  </div>
</template>

<script>
import MainPromote from '@/components/MainPromote.vue'
import CarouselProducts from '@/components/CarouselProducts.vue'

export default {
  name: 'Main-content',
  components: {
    MainPromote,
    CarouselProducts
  },
  data(){
    return {

    };
  }
}
</script>

<style lang="less">
@import '@/less/main.less';


</style>
