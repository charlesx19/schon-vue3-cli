<template>
  <div id="main-content">
    <div class="container">
      <MainPromote></MainPromote>
      <CarouselProducts></CarouselProducts>
      <Brands></Brands>
    </div>
  </div>
</template>

<script>
import MainPromote from '@/components/MainPromote.vue'
import CarouselProducts from '@/components/CarouselProducts.vue'
import Brands from '@/components/Brands.vue'

export default {
  name: 'Main-content',
  components: {
    MainPromote,
    CarouselProducts,
    Brands
  },
  data(){
    return {

    };
  }
}
</script>

<style lang="less">
  @import '@/less/main.less';
  #main-content {
    padding-bottom: 100px;
  }


</style>
