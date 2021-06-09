<template>
  <div class="header-top">
    <div class="container">
      <div class="row header-top-row">
        <div class="col-6 contact-info">
          <a href="tel:+1-555-333-22-11" class="phone">
            <div>
              <i class="fas fa-phone"></i>
              +1 (555) 333 22 11
            </div>
          </a>
          <a href="mailto:info@schon.chairs" class="mail">
            <div>
              <i class="far fa-envelope"></i>
              info@schon.chairs
            </div>
          </a>
        </div>
        <div class="col-6 order-info">
          <a href="#">
            <div>order track</div>
          </a>
          <a href="#">
            <div>my account</div>
          </a>
          <a href="#">
            <div>checkout</div>
          </a>
        </div>
      </div>
    </div>
  </div>
  <Header></Header>
    <router-view/>
  <Footer></Footer>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  },
  data(){
    return {

    };
  },
}
</script>


<style lang="less">
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@100;300;400;500;700;900&display=swap');
  @import '@/less/main.less';

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
    list-style: none;
    // font-family: sans-serif, Arial, Helvetica;
    font-family: 'Noto Sans TC', sans-serif;
  }
  .header-top {
    background: @header-top-gray;
    .header-top-row {
      color: #A1A1A1;
      align-items: center;
      a {
        display: inline-block;
        padding: 10px;
        color:#A1A1A1;
        font-size: 12px;
        font-weight: 500;
        letter-spacing: 2px;
        &:hover {
          text-decoration: none;
          background: @header-top-hover;
        }
        svg {
          width: 0.8rem;
        }
        div {
          transform: scale(0.9);
        }
      }
      .contact-info {
      }
      .order-info {
        text-align: right;
        a {
          text-transform: capitalize;
        }
      }
    }
  }

</style>
