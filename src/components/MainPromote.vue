<template>
  <div class="row">
    <a href="#" class="col-12 col-md-6 main-banner">
      <div class="box">
        <div class="info">
          <p class="subtitle">furniture designs ideas</p>
          <p class="title bold">new</p>
          <p class="title">collection</p>
          <p class="desc">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Culpa delectus beatae incidunt maxime earum! Aut?</p>
          <p class="price">$ 79.00</p>
        </div>
        <img src="~@/img/banner05.jpg" alt="products">
      </div>
    </a>
    <a href="#" class="col-12 col-md-6 col-lg-3 p-0 pt-3 px-lg-3 pl-md-3 pt-md-0 banner-01">
      <div class="box">
        <img src="~@/img/banner06.jpg" alt="products">

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
    <div class="col-12 col-lg-3 banner-02-03">
      <div class="row">
        <a href="#" class="col-12 banner-02 pt-3 pt-lg-0">
          <div class="box">
            <div class="info">
              <div class="title">{{ products["banner02"]["title"] }}</div>
              <div class="star-count">
                <i class="fas fa-star" v-for="count in products['banner02']['star']" :key="count"></i>
                <i class="far fa-star"></i>
              </div>
              <div class="price">{{ "$ " + products["banner02"]["price"] }}</div>
              <div class="shop-now">
                shop now
              </div>              
            </div>
          </div>
        </a>
        <a href="#" class="col-12 banner-03">
          <div class="box">
            <div class="info">
              <div class="title">{{ products["banner03"]["title"] }}</div>
              <div class="star-count">
                <i class="fas fa-star" v-for="count in products['banner03']['star']" :key="count"></i>
                <i class="far fa-star"></i>
              </div>
              <div class="price">{{ "$ " + products["banner03"]["price"] }}</div>
              <div class="dPrice">{{ "$ " + products["banner03"]["dPrice"] }}</div>
              <div class="shop-now">
                hurry up
                <span>
                  <i class="fas fa-chevron-right"></i>
                </span>
              </div>
            </div>
          </div>
        </a>
      </div>
    </div>
  </div>
  <div class="row">
    <div class="col-12 col-lg-4 banner-04-05">
      <div class="row">
        <a href="#" class="col-12 col-sm-6 col-lg-12 banner-04">
          <div class="box">
            <div class="info">
              <div class="subtitle">{{ products["banner04"]["subtitle"] }}</div>
              <div class="title">{{ products["banner04"]["title"] }}</div>
              <div class="shop-now">
                shop now
                <span>
                  <i class="fas fa-chevron-right"></i>
                </span>
              </div>
            </div>
          </div>
        </a>
        <a href="#" class="col-12 col-sm-6 col-lg-12 banner-05">
          <div class="box">
            <div class="info">
              <div class="subtitle">{{ products["banner05"]["subtitle"] }}</div>
              <div class="title">{{ products["banner05"]["title"] }}</div>
              <div class="shop-now">
                shop now
                <span>
                  <i class="fas fa-chevron-right"></i>
                </span>
              </div>
            </div>
          </div>
        </a>
      </div>
    </div>
    <div class="col-12 col-lg-8 carousel-banner">
      <div class="box">
        <div id="carousel" class="carousel slide" data-ride="carousel">
          <ol class="carousel-indicators">
            <li data-target="#carousel" data-slide-to="0" class="active"></li>
            <li data-target="#carousel" data-slide-to="1"></li>
            <li data-target="#carousel" data-slide-to="2"></li>
          </ol>
          <div class="carousel-inner">
            <!-- <div class="carousel-item active" v-for='item in products["caraselBanner"]' :key="item['title']">
              <div class="inner-box">
                <img src="~@/img/banner13.jpg" class="d-block" alt="...">
                <div class="subtitle">{{ item["subtitle"] }}</div>
                <div class="bigTitle">{{ item["bigTitle"] }}</div>
                <div class="title">{{ item["title"] }}</div>
                <div class="desc">{{ item["description"] }}</div>
              </div>
            </div> -->
            <div class="carousel-item active">
              <a href="#" class="inner-box item01">
                <div class="carousel-caption">
                  <div class="subtitle">{{ products["caraselBanner"][0]["subtitle"] }}</div>
                  <div class="bigTitle">{{ products["caraselBanner"][0]["bigTitle"] }}</div>
                  <div class="title">{{ products["caraselBanner"][0]["title"] }}</div>
                  <div class="desc">{{ products["caraselBanner"][0]["description"] }}</div>
                </div>
                <img src="~@/img/banner13.jpg" class="d-block" alt="...">
              </a>
            </div>
            <div class="carousel-item">
              <a href="#" class="inner-box item02">
                <div class="carousel-caption">
                  <div class="subtitle">{{ products["caraselBanner"][1]["subtitle"] }}</div>
                  <div class="bigTitle">{{ products["caraselBanner"][1]["bigTitle"] }}</div>
                  <div class="title">{{ products["caraselBanner"][1]["title"] }}</div>
                  <div class="desc">{{ products["caraselBanner"][1]["description"] }}</div>
                </div> 
                <img src="~@/img/IndoorRattanArmchair.jpg" class="d-block" alt="...">            
              </a>  
            </div>
            <div class="carousel-item">
              <a href="#" class="inner-box item03">
                <div class="carousel-caption">
                  <div class="subtitle">{{ products["caraselBanner"][2]["subtitle"] }}</div>
                  <div class="bigTitle">{{ products["caraselBanner"][2]["bigTitle"] }}</div>
                  <div class="title">{{ products["caraselBanner"][2]["title"] }}</div>
                  <div class="desc">{{ products["caraselBanner"][2]["description"] }}</div>
                </div>
                <img src="~@/img/RabieMadaciArmchair.jpg" class="d-block" alt="...">                
              </a>
            </div>
          </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>

export default {
  name: 'MainPromote',
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
          subtitle: "",
          title: "acrylic fabric bean bag",
          star: 3,
          price: "99.00",
          dPrice: "",
          url: "#"
        },
        banner03:{
          subtitle: "",
          title: "chiar with armrests",
          star: 3,
          price: "129.00",
          dPrice: "99.00",
          url: "#"
        },
        banner04:{
          subtitle: "chairs",
          title: "zio dining chair",
          price: "",
          dPrice: "",
          url: "#"
        },
        banner05:{
          subtitle: "accessories / lighting",
          title: "totem floor lamp",
          price: "",
          dPrice: "",
          url: "#"
        },
        caraselBanner: [
          {
            subtitle: "furniture designs ideas",
            bigTitle: "upholstered fabric",
            title: "counter stool",
            description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia, laborum?",
            url: "#"
          },
          {
            subtitle: "furniture designs ideas",
            bigTitle: "indoor rattan",
            title: "armchair",
            description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia, laborum?",
            url: "#"
          },
          {
            subtitle: "furniture designs ideas",
            bigTitle: "stylish orange",
            title: "plastic chair",
            description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia, laborum?",
            url: "#"
          }                  
        ]
      }
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

  @keyframes upDownMove {
    0% {
      transform: translateY(0px);
    }
    25% {
      transform: translateY(-8px);
    }
    50% {
      transform: translateY(3px);
    }
    100% {
      transform: translateY(0px);
    }

  }

  #main-content {
    .main-banner {
      padding: 0;
      height: 563px;
      width: auto;
      &:hover {
        p {
          text-decoration: none;
        }
      }
      .box {
        position: relative;
        display: flex;
        justify-content: flex-start;
        align-items: flex-end;
        height: 100%;
        width: 100%;
        padding: 76px 60px;
        // background-image: url("~@/img/banner05.jpg");
        // background-size: 100%, 100%;
        // background-repeat: no-repeat;
        .info {
          z-index: 100;
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
        img {
          position: absolute;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
        }
      }
    }
    .shop-now {
      width: fit-content;
      font-size: 13px;
      font-weight: 700;
      text-transform: uppercase;
    }
    .banner-01 {
      padding: 0 20px;
      height: 563px;
      &:hover .box .shop-now-box .shop-now {
        span {
          animation: arrow-move 1s ease-out infinite;
        }
      }
      * {
        position: relative;
      }
      .row {
        flex-direction: column;
      }
      .box {
        position: relative;
        padding: 30px 25px;
        height: 100%;
        // background-image: url("~@/img/banner06.jpg");
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
              svg {
                transform: translate(1px, -1px);
              }
            }
          }
        }
        img {
          position: absolute;
          display: block;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
          mix-blend-mode: multiply;
        }
      }
    }
    .banner-02-03 {
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
        background-size: inherit;
        background-repeat: no-repeat;
        background-blend-mode: multiply;
      }
      .title {
        width: 80%;
        font-size: 17px;
        font-weight: 700;
        text-transform: uppercase;
        letter-spacing: 2px;
      }
      .star-count {
        svg {
          margin: 0 1px;
          width: 0.7rem;
          color: #c8a760;
        }
      }
      // // Small devices (landscape phones, 576px and up)
      // @media (min-width: 576px) { ... }

      // // Medium devices (tablets, 768px and up)
      // @media (min-width: 768px) { ... }

      // // Large devices (desktops, 992px and up)
      // @media (min-width: 992px) { ... }

      // // Extra large devices (large desktops, 1200px and up)
      // @media (min-width: 1200px) { ... }
      .banner-02 {
        height: 50%;
        padding-bottom: 10px;
        &:hover {
          .box {
            .shop-now {
              animation: upDownMove 1s ease-in infinite;
            }
          }
        }
        .box {
          background-image: url("~@/img/banner07.jpg");
          background-position: left bottom;
          text-align: right;
          .title {
            margin-left: auto;
            color: @text-light-gray;
          }
          .star-count {
            margin-bottom: 25%;
          }
          .price {
            color: #991015;
            font-size: 24px;
            font-weight: 700;
          }
          .shop-now {
            padding: 2px 8px;
            margin-left: auto;
            margin-top: 6px;
            color: #fff;
            background: #2e2d32;
            transform: translateY(0px);
            transition: .5s all ease-in-out;
          }
        }
        @media (max-width: 1200px) {
          .box {
            background-size: 60%;
          }          
        }        
        @media (max-width: 992px) {
          .box {
            padding: 5% 10%;
            background-position: 25% bottom;
            background-size: 35%;
            .star-count {
              margin-bottom: 12%;
            }               
          }          
        }
        @media (max-width: 767px) {
          .box {
            background-size: 40%;
            .title {
              font-size: 30px;
            }
            .star-count {
              margin-bottom: 3%;
            }       
          }
        }        
      }
      .banner-03 {
        height: 50%;
        padding-top: 10px;
        &:hover .shop-now {
          span {
            animation: arrow-move 1s ease-out infinite;
          }
        }
        .box {
          background-image: url("~@/img/banner08.jpg");
          background-position: right;
          text-align: left;
          .title {
            margin-bottom: 25%;
            color: #2c3e66;
          }
          .price {
            color: @text-light-gray;
            font-size: 14px;
            font-weight: 700;
            text-decoration: line-through;
          }
          .dPrice {
            margin-bottom: 10px;
            color: #2c3e66;
            font-size: 24px;
            font-weight: 700;
          }
          .shop-now {
            color: #2c3e66;
            span {
              display: inline-block;
              margin-left: 10px;
              width: 23px;
              height: 23px;
              text-align: center;
              line-height: 23px;
              border: 1px solid #2c3e66;
              border-radius: 50%;
              svg {
                transform: translate(1px, -1px);
              }
            }
          }
        }
        @media (max-width: 1200px) {
          .box {
            background-size: 55%;
          }          
        }          
        @media (max-width: 992px) {
          .box {
            padding: 5% 10%;
            background-size: inherit;
            .title {
              margin-bottom: 10%;
            }       
          }
        }
        @media (max-width: 767px) {
          .box {
            .title {
              margin-bottom: 3%;
              font-size: 30px;
            }
          }
        }              
      }
    }
    .banner-04-05 {
      padding: 0;
      height: 579px;
      text-align: right;
      .box {
        background-color: @bg-light-gray;
        background-size: contain;
        background-repeat: no-repeat;
        background-blend-mode: multiply;
      }
      .row {
        height: 100%;
      }
      .subtitle {
        font-size: 14px;
        letter-spacing: 3px;
        text-transform: capitalize;
      }
      .title {
        font-size: 22px;
        font-weight: 700;
        text-transform: uppercase;
        letter-spacing: 2px;
      }
      .banner-04 {
        padding-top: 20px;
        padding-bottom: 10px;
        height: 40%;
        &:hover .shop-now {
          span {
            animation: arrow-move 1s ease-out infinite;
          }
        }
        .box {
          padding: 8%;
          height: 100%;
          background-color: #d0e9b0;
          background-image: url("~@/img/banner12.jpg");
          background-position: left center;
          background-blend-mode: multiply;
          color: #fff;
          .title {
            margin-bottom: 20%;
          }
          .shop-now {
            margin-left: auto;
            span {
              display: inline-block;
              margin-left: 10px;
              width: 23px;
              height: 23px;
              text-align: center;
              line-height: 23px;
              border: 1px solid #fff;
              border-radius: 50%;
              background: #b1de89;
              svg {
                transform: translate(1px, -1px);
              }
            }
          }
        }
      }
      @media (max-width: 992px) {
        .banner-04 {
          padding-right: 10px;
        }
      }      
      @media (max-width: 768px) {
        .banner-04 {
          height: 50%;
          .box {
            .title {
              margin-bottom: 23%;
            }
          }
        }
      }
      @media (max-width: 576px) {
        .banner-04 {
          padding-right: 15px;
        }
      }
      .banner-05 {
        padding-top: 10px;
        height: 60%;
        &:hover .shop-now {
          span {
            animation: arrow-move 1s ease-out infinite;
          }
        }
        .box {
          padding: 8%;
          height: 100%;
          background-image: url("~@/img/banner14.jpg");
          background-size: 89%;
          background-position: -230% bottom;
          background-blend-mode: multiply;
          .subtitle {
            color: #b7b7b7;
          }
          .title {
            color: #535353;
            margin-bottom: 60%;
          }
          .shop-now {
            margin-left: auto;
            color: #979797;
            span {
              display: inline-block;
              margin-left: 10px;
              width: 23px;
              height: 23px;
              text-align: center;
              line-height: 23px;
              border: 1px solid #979797;
              border-radius: 50%;
              svg {
                transform: translate(1px, -1px);
              }
            }
          }          
        }
      }
      @media (max-width: 1200px) {
        .banner-05 {
          .box {
            .title {
              width: 100%;
              margin-bottom: 70%;
            }
          }
        }
      }      
      @media (max-width: 992px) {
        .banner-05 {
          padding-left: 10px;
          padding-top: 20px;
          padding-bottom: 10px;
          .box {
            background-size: 74%;
            background-position: -80% bottom;            
            .title {
              width: 60%;
              margin: 10px 0 6% auto;
            }
          }
        }
      }
      @media (max-width: 767px) {
        .banner-05 {
          height: 50%;
          .box {
            background-size: 65%;
            background-position: -48% bottom;
            .title {
              width: 85%;
              margin-bottom: 18%;
            }
          }
        }
      }
      @media (max-width: 576px) {
        .banner-05 {
          padding-top: 10px;
        }
      }
      @media (max-width: 415px) {
        .banner-05 {
          .box {
            .title {
              width: 70%;
            }
          }
        }
      }
    }
    @media (max-width: 992px) {
      .banner-04-05 {
        height: 230px;
        .banner-04, .banner-05 {
          height: 100%;
        }
      }
    }
    @media (max-width: 576px) {
      .banner-04-05 {
        height: auto;
      }
    }
    .carousel-banner {
      padding-top: 20px;
      padding-right: 0;
      height: 579px;
      .box {
        height: 100%;
        background: @bg-light-gray;
        #carousel {
          height: 100%;
          .carousel-indicators {
            position: absolute;
            /* right: 0; */
            bottom: 7%;
            left: 0;
            z-index: 15;
            display: flex;
            justify-content: flex-start;
            padding-left: 0;
            /* margin-right: 15%; */
            margin-left: 8%;
            list-style: none;
            li {
              box-sizing: border-box;
              padding: 0;
              margin: 0 3px;
              width: 14px;
              height: 14px;
              border: 2px solid #999;
              border-radius: 50%;
              background: transparent;
            }
          }
          .carousel-inner {
            height: 100%;
            .carousel-item {
              height: 100%;
            }
            .inner-box {
              position: relative;
              display: block;
              height: 100%;
              padding: 8%;
              img {
                position: absolute;
                left: 0;
                top: 0;
                width: 100%;
                height: 100%;
                mix-blend-mode: multiply;
              }
              .subtitle {
                font-size: 14px;
                font-weight: 700;
                letter-spacing: 2px;
                text-transform: uppercase;                             
              }
              .bigTitle, .title {
                font-size: 44px;
                font-weight: 700;
                line-height: 3.5rem;
                letter-spacing: 1px;
                text-transform: capitalize;
              }
              .bigTitle {
                margin-top: 8px;
              }
              .title {
                margin-bottom: 8px;
                font-weight: 100;
              }
              .desc {
                width: 60%;
                font-size: 12px;
              }
              .carousel-caption {
                position: absolute;
                padding: 8% 8%;
                width: 100%;
                height: 100%;
                left: 0;
                top: 0;
                z-index: 10;
              }
              &.item01 {
                .carousel-caption {
                  text-align: left;
                }
                .subtitle {
                  color: #6a6a6a;
                }
                .bigTitle, .title, .desc {
                  color: #535353;
                }
              }
              &.item02 {
                .carousel-caption {
                  text-align: right;
                }
                .subtitle {
                  color: #fff;
                }
                .bigTitle, .title, .desc {
                  color: #fff;
                }
                .desc {
                  margin-left: auto;
                }
              }
              &.item03 {
                .carousel-caption {
                  text-align: left;
                }
                .subtitle {
                  color: #ffa052;
                }
                .bigTitle, .title {
                  font-size: 36px;
                  color: #ff7300;
                }
                .desc {
                  width: 50%;
                  color: #ffa052;
                }
              }                              
            }
          }
        }
      }
    }
    @media (max-width: 992px) {
      .carousel-banner {
        padding-left: 0;
        padding-top: 10px;
        height: 590px;
      }
    }
    @media (max-width: 767px) {
      .carousel-banner {
        height: 400px;
      }
    }    
    @media (max-width: 539px) {
      .carousel-banner {
        height: 340px;
      }
    }      
  }
  
</style>
