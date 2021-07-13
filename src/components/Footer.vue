<template>
  <div id="footer">
    <div id="footer-top" class="container-fluid">
      <div class="container">
        <div class="row features">
          <div class=" item">
            <div class="row no-gutters">
              <div class="col-2 icon">
                <i class="fas fa-plane"></i>
              </div>
              <div class="col-10">
                <div class="info">
                  <div class="title">free shipping</div>
                  <div class="desc">Free shipping on all US order</div>
                </div>
              </div>
            </div>
          </div>
          <div class=" item">
            <div class="row no-gutters">
              <div class="col-2 icon">
                <i class="far fa-life-ring"></i>
              </div>
              <div class="col-10">
                <div class="info">
                  <div class="title">support 24/7</div>
                  <div class="desc">We support 24 hours a day</div>
                </div>
              </div>
            </div>
          </div>          
          <div class=" item">
            <div class="row no-gutters">
              <div class="col-2 icon">
                <i class="fas fa-box-open"></i>
              </div>
              <div class="col-10">
                <div class="info">
                  <div class="title">gift cards</div>
                  <div class="desc">Give perfect gift</div>
                </div>
              </div>
            </div>
          </div>
          <div class=" item">
            <div class="row no-gutters">
              <div class="col-2 icon">
                <i class="far fa-money-bill-alt"></i>
              </div>
              <div class="col-10">
                <div class="info">
                  <div class="title">payment 100% secure</div>
                  <div class="desc">Payment 100% secure</div>
                </div>
              </div>
            </div>
          </div>          
        </div>
        <div class="row quick-links">
          <div class="col-3 basic-info">
            <div class="logo">
              <img src="@/img/logo_gray.svg" alt="">
            </div>
            <div class="desc">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maxime, quo!
            </div>
            <div class="address">
              <div class="row no-gutters">
                <div class="col-1 icon">
                  <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="col-11 info">
                  Connaugt Road Central Suite 18B, 148 New Yankee
                </div>
              </div>
            </div>
            <div class="phone">
              <a class="row no-gutters" href="tel:+1-555-333-22-11">
                <div class="col-1">
                  <i class="fas fa-phone-alt"></i>
                </div>
                <div class="col-11 info">
                  +1 (555) 333 22 11
                </div>
              </a>
            </div>
            <div class="mail">
              <a class="row no-gutters" href="mailto:info@schon.chairs">
                <div class="col-1">
                  <i class="far fa-envelope"></i>
                </div>
                <div class="col-11 info">
                  info@schon.chair
                </div>
              </a>
            </div>            
          </div>
          <div class="col-2 quick-link category">
            <div class="box">
              <div class="title">categories</div>
              <ul>
                <li><a href="#">chairs</a></li>
                <li><a href="#">sofas</a></li>
                <li><a href="#">living</a></li>
                <li><a href="#">bedroom</a></li>
                <li><a href="#">tables</a></li>
                <li><a href="#">new</a></li>
              </ul>
            </div>
          </div>
          <div class="col-2 quick-link information">
            <div class="box">
              <div class="title">information</div>
              <ul>
                <li><a href="#">about us</a></li>
                <li><a href="#">contact us</a></li>
                <li><a href="#">terms &amp; condition</a></li>
                <li><a href="#">privacy policy</a></li>
                <li><a href="#">customer service</a></li>
                <li><a href="#">FAQs</a></li>
              </ul>
            </div>    
          </div>
          <div class="col-2 quick-link account">
            <div class="box">
              <div class="title">account</div>
              <ul>
                <li><a href="#">my account</a></li>
                <li><a href="#">order tracking</a></li>
                <li><a href="#">wish list</a></li>
                <li><a href="#">shopping cart</a></li>
                <li><a href="#">checkout</a></li>
              </ul> 
            </div>            
          </div>
          <div class="col-3 social-media">
            <div class="box">
              <div class="signUpNewsLetter">
                <div class="title">sign up newsletter</div>
                <div class="emailInputBox">
                  <div class="input-group">
                    <input type="text" class="emailInput form-control" placeholder="Your e-mail" aria-label="Your e-mail" aria-describedby="basic-addon2">
                    <div class="input-group-append">
                      <button class="subscribeButton btn btn-outline-secondary" type="button">Subscribe</button>
                    </div>
                  </div>
                </div>
              </div>
              <div class="followUs">
                <div class="title">follow us</div>
                <ul class="socialsIcon">
                  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
                  <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
                  <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
                  <li><a href="#"><i class="fab fa-whatsapp"></i></a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="footer-bottom" class="container">
      <div class="row">
        <div class="col-6 logo">
          &copy;
          <img src="@/img/logo.svg" alt="logo">
          -All rights Reserved
        </div>
        <div class="col-6 payment">
          <i class="fab fa-cc-visa"></i>
          <i class="fab fa-cc-paypal"></i>
          <i class="fab fa-cc-mastercard"></i>
          <i class="fab fa-cc-discover"></i>
          <i class="fab fa-amazon"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Footer',
  components: {
  }
}
</script>

<style lang="less">
  @import '@/less/main.less';

  #footer {
    #footer-top {
      padding: 3rem 0;
      background: #f6f6f6;
      .features {
        flex-wrap: nowrap;
        padding-bottom: 3rem;
        border-bottom: 1px solid #e0e0e0;
        .item {
          width: fit-content;
          height: auto;
          .icon {
            line-height: 1rem;
            svg {
              width: 100%;
              height: auto;
              color: #838182;
            }
          }
          .info {
            padding-left: 10px;
            .title {
              font-size: 14px;
              font-weight: 700;
              color: #353535;
              letter-spacing: 1px;
              text-transform: uppercase;
            }
            .desc {
              font-size: 12px;
              font-weight: 300;
              color: #353535;
            }
          }
          &:nth-child(1) {
            svg {
              transform: rotate(-45deg);
            }
          }
        }
      }
      .quick-links {
        padding-top: 3rem;
        align-items: flex-start;
        .basic-info, a {
          font-size: 12px;
          font-weight: 500;
          color: #868686;
          .info {
            padding-left: 5px;
          }
          .logo {
            margin-bottom: 27px;
            img {
              width: 115px;
              height: auto;
            }
          }
          .desc {
            margin-bottom: 37px;
            word-break: break-all;
          }
          .address {
            margin-bottom: 27px;
          }
        }
        .quick-link {
          text-align: center;
          .box {
            width: fit-content;
            margin: auto;
            text-align: left;
            .title {
              margin-bottom: 1.5rem;
              font-size: 14px;
              font-weight: 700;
              text-transform: capitalize;
            }
            li {
              margin-bottom: 1rem;
              a {
                font-size: 12px;
                font-weight: 500;
                text-transform: capitalize;
              }
            }
          }
        }
        .social-media {
          text-align: right;
          .title {
            margin-bottom: 1.5rem;
            font-size: 14px;
            font-weight: 700;
            text-transform: capitalize;
          }
          .signUpNewsLetter {
            margin-bottom: 3rem;
            .emailInputBox {
              height: 3rem;
              .emailInput{
                padding-left: 1.5rem;
                font-size: 12px;
                font-weight: 300;
                border-top-left-radius: 1.25rem;
                border-bottom-left-radius: 1.25rem;
              }
              .subscribeButton {
                font-size: 12px;
                font-weight: 300;
                border: none;
                color: #fff;
                background: #696969;
                border-top-right-radius: 1.25rem;
                border-bottom-right-radius: 1.25rem;
              }
            }
          }
          .followUs {
            .title {
              margin-bottom: 1rem;
            }
            .socialsIcon {
              display: flex;
              justify-content: flex-end;
              align-items: center;
              li {
                margin-left: 0.7rem;
                svg {
                  font-size: 16px;
                }
              }
            }
          }
        }
      }
    }
    #footer-bottom {
      padding: 1.5rem 0;
      .logo {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        font-size: 12px;
        font-weight: 300;
        img {
          margin: 0 0.3rem;
          width: 50px;
          height: auto;
        }
      }
      .payment {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        font-size: 12px;
        font-weight: 300;
        svg {
          margin-left: 1.5rem;
          font-size: 24px;
          color: @main-gray;
        }
      }
    }
  }


</style>
