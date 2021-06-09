<template>
  <div id="header">
    <!-- <div id="nav">
      <router-link class="test" to="/">Home</router-link> |
      <router-link class="test" to="/about">About</router-link>
    </div> -->
    <div class="container">
      <div class="row">
        <div class="col-3">
          <div class="logo-container">
            <a href="#">
              <img src="@/img/logo.svg" alt="logo">
            </a>
          </div>
        </div>
        <div class="col-9">
          <div class="row">
            <div id="nav" class="col-8">
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
            <div class="other col-4">
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
  
</style>
