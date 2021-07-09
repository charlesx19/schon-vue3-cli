<template>
  <div id="otherProducts" class="row items">
    <div class="item col-4" v-for="item in otherProducts" :key="item.title">
      <img :src="item.bgImg" :alt="item.title">
      <div class="infos">
        <div class="info">
          <div class="category">{{ item.category }}</div>
          <div class="title">{{ item.title }}</div>
        </div>
        <div class="linkToProductPage">
          view
          <span>
            <i class="fas fa-angle-right"></i>
          </span>
        </div>         
      </div>     
    </div>
  </div>

</template>

<script>
import bgImg01 from "@/img/banner09.jpg"
import bgImg02 from "@/img/banner10.jpg"
import bgImg03 from "@/img/banner11.jpg"

export default {
  name: 'OtherProducts',
  components: {
  },
  data(){
    return {
      otherProducts:[
        {
          category: "Wall Decor",
          title: "CLOCKs",
          url: "#",
          // bgImg: "https://source.unsplash.com/500x300/?furniture,clock"
          bgImg: bgImg01
        },
        {
          category: "Coffee Tables",
          title: "S.O.S. BLOCKS",
          url: "#",
          bgImg: bgImg02
        },
        {
          category: "Floor Lamps",
          title: "ROCKing LAMP",
          url: "#",
          bgImg: bgImg03
        },                
      ],
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

  #otherProducts {
    padding-top: 1.5rem;
    .item {
      position: relative;
      padding: 0;
      height: 200px;
      overflow: hidden;
      &:nth-child(1), &:nth-child(3) {
        background: #f8f8f8;
      }
      &:nth-child(2) {
        background: #f1f1f1;
      }      
      img {
        position: absolute;
        right: 0px;
        bottom: 0px;
        height: 100%;
        width: auto;
        transform: scale(0.7) translate(20%, 10%);
        mix-blend-mode: multiply;
      }
      .infos {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;
        width: 100%;
        padding: 10% 10%;
        .info {
          .category {
            font-size: 13px;
            font-weight: 300;
            color: #c0c0c0;
            letter-spacing: 2px;
          }
          .title {
            font-size: 20px;
            font-weight: 700;
            color: #535353;
            letter-spacing: 2px;
          }
        }
        .linkToProductPage {
          font-size: 12px;
          font-weight: 500;
          text-transform: uppercase;
          letter-spacing: 2px;
          color: #979797;
          span {
            display: inline-block;
            margin-left: 0.2rem;
            width: 20px;
            height: 20px;
            line-height: 20px;
            text-align: center;
            border: 1px solid #979797;
            border-radius: 50%;
            svg {
              font-size: 12px;
              transform: translateY(-1px);
            }
          }
        }
      }
    }
    @media (max-width: 992px) {
      .item {
        img {
          width: 100%;
          height: auto;
          transform: scale(0.6) translate(35%, 30%);
        }
      }
    }    
    @media (max-width: 767px) {
      .item {
        height: 320px;
        img {
          width: 100%;
          height: auto;
          transform: scale(1) translate(0, -50%);
        }
      }
    }
    @media (max-width: 530px) {
      .item {
        height: 200px;
        flex: 0 0 100%;
        max-width: 100%;
        img {
          transform: scale(0.6) translate(40%, 30%);
        }
      }
    }
  }
</style>
