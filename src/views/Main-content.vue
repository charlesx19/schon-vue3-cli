<template>
  <div id="main-content">
    <div class="container">
      <MainPromote></MainPromote>
    </div>
  </div>
</template>

<script>
import MainPromote from '@/components/MainPromote.vue'

export default {
  name: 'Main-content',
  components: {
    MainPromote,
  },
  data(){
    return {
      products:{
        banner01:{
          subtitle: "sofas & armchairs",
          title: "3 seater leather sofa",
          price: "699.00",
          dPrice: "499.00",
          url: "#",
          // bgImg: "background-image: url('~@/img/banner06.jpg')"
        },
        banner02:{
          subtitle: "",
          title: "acrylic fabric bean bag",
          star: 3,
          price: "99.00",
          dPrice: "",
          url: "#"
        },
        banner03:{
          subtitle: "",
          title: "chair with armrests",
          star: 3,
          price: "129.00",
          dPrice: "99.00",
          url: "#"
        },
      }
    };
  }
}
</script>

<style lang="less">
@import '@/less/main.less';


</style>
