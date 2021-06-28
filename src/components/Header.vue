<template>
  <div id="header">
    <!-- <div id="nav">
      <router-link class="test" to="/">Home</router-link> |
      <router-link class="test" to="/about">About</router-link>
    </div> -->
    <div id="nav-mobile" class="row no-gutters d-flex d-md-none">
      <div class="col-3 item home">
        <div class="box">
          <i class="fas fa-home"></i>
        </div>
      </div>
      <div class="col-3 item shopping-car">
        <div class="box">
          <i class="fas fa-shopping-cart"></i>
        </div>
      </div>
      <div class="col-3 item account">
        <div class="box">
          <i class="fas fa-user-circle"></i>
        </div>
      </div>
      <div class="col-3 item menu">
        <div class="box">
          <i class="fas fa-bars"></i>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-12 col-lg-3">
          <div class="logo-container">
            <a href="#">
              <img src="@/img/logo.svg" alt="logo">
            </a>
          </div>
        </div>
        <div class="col-lg-9 d-none d-md-block">
          <div class="row">
            <div id="nav" class="col-12 col-md-8">
              <ul>
                <li><a href="#">home</a></li>
                <li class="down-arrow">
                  <a href="#">
                    products
                  <i class="fas fa-chevron-down"></i>
                  </a>
                </li>
                <li><a href="#">about</a></li>
                <li><a href="#">blog</a></li>
                <li><a href="#">contact</a></li>
              </ul>
            </div>
            <div class="other col-12 col-md-4">
              <div class="search">
                <i class="fas fa-search"></i>
              </div>
              <div class="shopping-cart full">
                <div class="d-flex align-items-center">
                  <span class="mr-2 shopping-bag-icon-container">
                    <i class="fas fa-shopping-bag"></i>
                  </span>
                  <span>
                    <div class="shopping-cart-title">shopping cart</div>
                    <div class="order-info">
                      <span class="mr-2">3 items</span>
                      <span>$74.00</span>
                    </div>
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
  
</template>

<script>

export default {
  name: 'Header',
  components: {
  }
}
</script>

<style lang="less" scope>
  @import '@/less/main.less';

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
    list-style: none;
  }

  .row {
    align-items: center;
  }

  #header {
    padding: 30px 0 40px 0;
    .logo-container {
      width: 45%;
      img {
        width: 100%;
      }
    }
    @media (max-width: 992px) {
      .logo-container {
        width: 100%;
        text-align: center;
        img {
          margin-bottom: 3%;
          width: 150px;
          height: auto;
        }
      }
    }
    @media (max-width: 767px) {
      .logo-container {
        img {
          margin-bottom: 0;
        }
      }
    }
    #nav-mobile {
      position: fixed;
      bottom: -2px;
      left: 0;
      width: 100vw;
      height: 60px;
      text-align: center;
      background: #fff;
      z-index: 999;
      .item {
        height: 100%;
        .box {
          height: 100%;
          font-size: 24px;
          font-weight: 700;
          letter-spacing: 2px;
          line-height: 3.5rem;
          box-shadow: inset 0px 3px 3px rgba(0,0,0,.1);
          background: #d8d8d8;
          color: @main-gray;
        }
      }
    }
    #nav {
      ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin: 0;
        li {
          position: relative;
          margin: 0 13px;
          &:hover {
            &:after {
              width: 100%;
            }
          }
          &:after {
            position: absolute;
            content: "";
            left: 0;
            bottom: -1px;
            width: 0%;
            height: 1.5px;
            background: @main-gray;
            transition: .3s all ease-in-out;
          }
          &.down-arrow {
            svg {
              margin-left: 0.2rem;
              width: 0.5rem;
            }
          }
          a {
            font-size: 15px;
            text-transform: uppercase;
            color: @main-gray;
            &:hover {
              text-decoration: none;
            }
          }
        }
      }
    }
    .other {
      display: flex;
      justify-content: space-around;
      align-items: center;
      height: 100%;
      svg {
        width: 1.3rem;
        height: 1.3rem;
      }
      .search {
        position: relative;
        color: @main-gray;
        cursor: pointer;
        &:hover {
          &:after {
           transform: scaleX(1);
          }
        }
        &:after {
          position: absolute;
          content: '';
          left: 0;
          bottom: 0;
          width: 100%;
          height: 1.5px;
          transform: scaleX(0);
          transform-origin: 0;
          transition: .3s all ease-in-out;
          background: @main-gray;
        }
      }
      .shopping-cart {
        text-transform: uppercase;
        color: @main-gray;
        cursor: pointer;
        .shopping-cart-title{
          font-size: 13px;
          font-weight: 700;
          color: @main-gray;
          letter-spacing: 1px;
        }
        .order-info {
          font-size: 1px;
          font-weight: 400;
          color: @main-gray;
          letter-spacing: 1px;
        }
      }
    }
  }
  @media (max-width: 767px) {
    #header {
      padding: 4% 0;
    }
  }
</style>
