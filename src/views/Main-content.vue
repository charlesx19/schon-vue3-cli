<template>
  <div id="main-content">
    <div class="container">
      <div class="row">
        <a href="#" class="col-6 banner-01">
          <div class="box">
            <div class="info">
              <p class="subtitle">furniture designs ideas</p>
              <p class="title bold">new</p>
              <p class="title">collection</p>
              <p class="desc">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Culpa delectus beatae incidunt maxime earum! Aut?</p>
              <p class="price">$ 79.00</p>
            </div>
          </div>
        </a>
        <a href="#" class="col-3 banner-02">
          <div class="box">
            <div class="title-box">
              <p class="subtitle">{{ products["banner01"]["subtitle"] }}</p>
              <p class="title">{{ products["banner01"]["title"] }}</p>
            </div>
            <div class="price-circle">
              <div class="price">{{ "$ " + products["banner01"]["price"] }}</div>
              <div class="dPrice">{{ "$ " + products["banner01"]["dPrice"] }}</div>
            </div>
            <div class="shop-now-box">
              <div class="shop-now">
                shop now
                <span>
                  <i class="fas fa-chevron-right"></i>
                </span>
              </div>
            </div>
          </div>
        </a>
        <div class="col-3 banner-03-04">
          <div class="row">
            <a href="#" class="col-12 banner-03">
              <div class="box">
                <div class="title">acrylic fabric bean bag</div>
                <div class="star-count">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </a>
            <a href="#" class="col-12 banner-04">
              <div class="box"></div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'Main-content',
  components: {
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
          subtitle: "sofas & armchairs",
          title: "3 seater leather sofa",
          price: "699.00",
          dPrice: "499.00",
          url: "#"
        },
        banner03:{
          subtitle: "sofas & armchairs",
          title: "3 seater leather sofa",
          price: "699.00",
          dPrice: "499.00",
          url: "#"
        },
      }
    };
  }
}
</script>

<style lang="less">
@import '@/less/main.less';

  @keyframes arrow-move {
    0% {
      transform: translateX(0px);
    }
    30% {
      transform: translateX(20px);
    }
    100% {
      transform: translateX(0px);
    }
  }

  #main-content {
    .banner-01 {
      padding: 0;
      height: 563px;
      &:hover {
        p {
          text-decoration: none;
        }
      }
      .box {
        display: flex;
        justify-content: flex-start;
        align-items: flex-end;
        height: 100%;
        padding: 76px 60px;
        background-image: url("~@/img/banner05.jpg");
        .info {
          * {
            margin: 0;
            padding: 0;
          }
          width: 300px;
          .subtitle {
            padding: 3px 10px;
            width: fit-content;
            font-size: 14px;
            font-weight: 600;
            text-transform: uppercase;
            background: rgba(255,255,255,.1);
            color: #fff;
            letter-spacing: 2px;
            transform: translateX(-10px);
          }
          .title {
            margin: 10px 0;
            font-size: 42px;
            text-transform: capitalize;
            color: #fff;
            line-height: 2.5rem;
            letter-spacing: 2px;
            &.bold {
              font-weight: 900;
            }
          }
          .desc {
            margin: 15px 0;
            font-size: 12px;
            font-weight: 500;
            color: #fff;
          }
          .price {
            font-size: 26px;
            font-weight: 600;
            letter-spacing: 1px;
            color: #fff;
          }
        }
      }
    }
    .banner-02 {
      padding: 0 20px;
      height: 563px;
      &:hover .box .shop-now-box .shop-now {
        span {
          transform: translateX(0px);
          animation: arrow-move .7s ease-out infinite;
        }
      }
      .row {
        flex-direction: column;
      }
      .box {
        position: relative;
        padding: 30px 25px;
        height: 100%;
        background-image: url("~@/img/banner06.jpg");
        .title-box {
          .subtitle {
          font-size: 14px;
          font-weight: 600;
          text-transform: uppercase;
          color: #fff;
          letter-spacing: 2px;
          }
          .title {
            font-size: 22px;
            font-weight: 700;
            text-transform: capitalize;
            color: #fff;
          }
        }
        .price-circle {
          position: relative;
          margin-left: auto;
          width: 130px;
          height: 130px;
          top: 135px;
          border-radius: 50%;
          text-align: center;
          line-height: 130px;
          background: #62c5de;
          .price {
            position: absolute;
            left: 50%;
            top: -20%;
            font-size: 16px;
            text-decoration: line-through;
            color: rgba(255, 255, 255, .3);
            transform: translateX(-50%);
          }
          .dPrice {
            font-size: 24px;
            font-weight: 500;
            color: #fff;
          }
        }
        .shop-now-box {
          .shop-now {
            margin-top: 230px;
            font-size: 13px;
            font-weight: 700;
            text-transform: uppercase;
            color: #fff;
            span {
              display: inline-block;
              margin-left: 10px;
              width: 23px;
              height: 23px;
              text-align: center;
              line-height: 23px;
              border: 1px solid #fff;
              border-radius: 50%;
            }
          }
        }
      }
    }
    .banner-03-04 {
      padding: 0;
      height: 563px;
      .row {
        height: 100%;
      }
      .box {
        position: relative;
        padding: 30px 25px;
        height: 100%;
        background-color: @bg-light-gray;
        background-image: url("~@/img/banner08.jpg");
        background-size: cover;
        background-size: inherit;
        background-repeat: no-repeat;
        background-blend-mode: multiply;
      }
      .banner-03 {
        height: 50%;
        padding-bottom: 10px;
        .box {
          background-image: url("~@/img/banner07.jpg");
          background-position: left bottom;
        }
      }
      .banner-04 {
        height: 50%;
        padding-top: 10px;
        .box {
          background-image: url("~@/img/banner08.jpg");
          background-position: right;
        }
      }
    }
  }
</style>
