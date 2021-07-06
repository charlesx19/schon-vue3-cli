<template>
  <div id="brands" class="row">
    <div class="col-12 title">
      brands
      <span>furniture</span>
    </div>
    <div class="col-12 p-0">
      <div class="row">
        <div class="col-1 controller-prev" href="#brandsCarousel" role="button" data-slide="prev">
          <i class="fas fa-angle-left"></i>
        </div>
        <div class="col-10">
          <div id="brandsCarousel" class="carousel slide" data-ride="carousel" data-interval="false">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <div class="row">
                  <div class="col-2 item"><img src="@/img/brand-01.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-02.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-03.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-04.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-05.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-06.jpg" alt="brand"></div>
                </div>
              </div>
              <div class="carousel-item">
                <div class="row">
                  <div class="col-2 item"><img src="@/img/brand-04.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-05.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-06.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-07.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-08.jpg" alt="brand"></div>
                  <div class="col-2 item"><img src="@/img/brand-09.jpg" alt="brand"></div>
                </div>
              </div>
            </div>
          </div>          
        </div>
        <div class="col-1 controller-next" href="#brandsCarousel" role="button" data-slide="next">
          <i class="fas fa-angle-right"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Brands',
  components: {
  },
  data(){
    return {
    };
  },
  methods: {
  },
  mounted(){
  },
}
</script>

<style lang="less" scope>
  @import '@/less/main.less';

  #brands {
    padding-top: 3rem;
    .title {
      padding: 0;
      padding-bottom: 2rem;
      font-size: 22px;
      font-weight: 900;
      letter-spacing: 2px;
      color: #3a3a3a;
      text-transform: uppercase;
      span {
        font-size: 14px;
        font-weight: 700;
        letter-spacing: 3px;
        color: #c3c3c3;
      }
    }
    .controller-next, .controller-prev {
      color: #c3c3c3;
      cursor: pointer;
    }
    .controller-next {
      text-align: right;
    }
    #brandsCarousel {
      .item {
        text-align: center;
        img {
          width: 80%;
          height: auto;
        }
      }
    }
  }


</style>
