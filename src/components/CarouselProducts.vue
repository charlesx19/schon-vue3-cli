<template>
  <div id="carouselProducts" class="row d-none d-lg-flex">
    <div class="col-12 controller">
      <!-- <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a> -->
      <div class="row no-gutters">
        <div class="col-8 filter-title">
          <span @click="featuredShow" :class="{active: featured}">featured</span>
          <span @click="latestShow" :class="{active: latest}">latest</span>
          <span @click="bestSellerShow" :class="{active: bestSeller}">best seller</span>
        </div>
        <div class="col-4">
          <div class="controller-box d-none d-lg-block">
            <div class="box">
              <a :href="'#' + controller" class="prev" role="button" data-slide="prev">
                <i class="fas fa-angle-left"></i>
              </a>
              <a :href="'#' + controller" class="next" role="button" data-slide="next">
                <i class="fas fa-angle-right"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-12 featuredProducts items " v-show="featured">
      <div id="featuredCarousel" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.featuredRow01" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.featuredRow02" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                          
            </div>
          </div>          
        </div>
      </div>      
    </div>  
    <div class="col-12 latestProducts items" v-show="latest">
      <div id="latestCarousel" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.latestRow01" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                    <img :src="item.bgImg" class="d-block" alt="...">
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.latestRow02" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                    <img :src="item.bgImg" class="d-block" alt="...">
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                          
            </div>
          </div>          
        </div>
      </div>      
    </div>
    <div class="col-12 bestSellerProducts items" v-show="bestSeller">
      <div id="bestSellerCarousel" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.bestSellerRow01" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item">
            <div class="row">
              <a href="#" class="item col-3" v-for="item in carouselProducts.bestSellerRow02" :key="item['name']">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                          
            </div>
          </div>          
        </div>
      </div>      
    </div>        
  </div>
  <!-- 行動版的carousel，瀏覽器寬度低於992時觸發顯示，並關閉原始版的carousel -->
  <div id="carouselProductsMobile" class="row d-flex d-lg-none">
    <div class="col-12 controller">
      <div class="row no-gutters">
        <div class="col-12 col-sm-8 filter-title">
          <span @click="featuredShow" :class="{active: featured}">featured</span>
          <span @click="latestShow" :class="{active: latest}">latest</span>
          <span @click="bestSellerShow" :class="{active: bestSeller}">best seller</span>
        </div>
        <div class="col-4 controller-box">
          <div class="">
            <div class="box">
               <a :href="'#' + controller + 'Mobile'" class="prev" role="button" data-slide="prev">
                <i class="fas fa-angle-left"></i>
              </a>
              <a :href="'#' + controller + 'Mobile'" class="next" role="button" data-slide="next">
                <i class="fas fa-angle-right"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-12 featuredProductsMobile items " v-show="featured">
      <div id="featuredCarouselMobile" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item" v-for="item in carouselProducts.featuredRow01" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item" v-for="item in carouselProducts.featuredRow02" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>                
        </div>
      </div>      
    </div>      
    <div class="col-12 latestProductsMobile items " v-show="latest">
      <div id="latestCarouselMobile" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item" v-for="item in carouselProducts.latestRow01" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item" v-for="item in carouselProducts.latestRow02" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>                
        </div>
      </div>      
    </div>  
    <div class="col-12 bestSellerProductsMobile items " v-show="bestSeller">
      <div id="bestSellerCarouselMobile" class="carousel slide" data-ride="carousel" data-interval="false">
        <div class="carousel-inner">
          <div class="carousel-item" v-for="item in carouselProducts.bestSellerRow01" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
              </a>                                                             
            </div>
          </div>
          <div class="carousel-item" v-for="item in carouselProducts.bestSellerRow02" :key="item['name']">
            <div class="row">
              <a href="#" class="item col-12">
                <div class="box">
                  <div class="imgBox">
                    <img :src="item.bgImg" class="d-block" alt="...">
                    <div class="quick-action-box row no-gutter">
                      <div class="add-to-cart col-6">
                        <i class="fas fa-shopping-bag"></i>
                      </div>
                      <div class="add-to-favorite col-6">
                        <i class="fas fa-heart"></i>
                      </div>
                    </div>                    
                  </div>
                  <div class="info">
                    <div class="star-count" :class="{ 'hide': item.starCount == 0}">
                      <i v-for="stars in item.starCount" :key="stars" class="fas fa-star"></i>
                      <i class="far fa-star"></i>
                    </div>
                    <div class="title">{{ item["title"] }}</div>
                    <div class="price">{{ "$ " + item["price"] }}</div>
                  </div>               
                </div>
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
  name: 'CarouselProducts',
  components: {
  },
  data(){
    return {
      carouselProducts:{
        featuredRow01:[
          {
            starCount: 3,
            title: "bombi chair",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,chair"
          },
          {
            starCount: 0,
            title: "marvelous modern 3 seater",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,table"
          },
          {
            starCount: 3,
            title: "chair with armrests",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,wood"
          },
          {
            starCount: 0,
            title: "product title-04",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,fashion"
          },                                                                    
        ],
        featuredRow02:[
          {
            starCount: 3,
            title: "product title-05",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,desk"
          },
          {
            starCount: 0,
            title: "product title-06",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,gold"
          },
          {
            starCount: 3,
            title: "product title-07",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,beauty"
          },
          {
            starCount: 0,
            title: "product title-08",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,shiny"
          },                                                                    
        ],
        latestRow01:[
          {
            starCount: 3,
            title: "latest product-01",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,chair"
          },
          {
            starCount: 0,
            title: "latest product-02",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,table"
          },
          {
            starCount: 3,
            title: "latest product-03",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,wood"
          },
          {
            starCount: 0,
            title: "latest product-04",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,fashion"
          },                                                                    
        ],
        latestRow02:[
          {
            starCount: 3,
            title: "latest product-05",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,desk"
          },
          {
            starCount: 0,
            title: "latest product-06",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,gold"
          },
          {
            starCount: 3,
            title: "latest product-07",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,beauty"
          },
          {
            starCount: 0,
            title: "latest product-08",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?design,shiny"
          },                                                                    
        ],  
        bestSellerRow01:[
          {
            starCount: 3,
            title: "bestSeller product-01",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,chair"
          },
          {
            starCount: 0,
            title: "bestSeller product-02",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,table"
          },
          {
            starCount: 3,
            title: "bestSeller product-03",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,wood"
          },
          {
            starCount: 0,
            title: "bestSeller product-04",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,fashion"
          },                                                                    
        ],
        bestSellerRow02:[
          {
            starCount: 3,
            title: "bestSeller product-05",
            price: "399.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,desk"
          },
          {
            starCount: 0,
            title: "bestSeller product-06",
            price: "599.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,gold"
          },
          {
            starCount: 3,
            title: "bestSeller product-07",
            price: "200.00",
            discount: 15,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,beauty"
          },
          {
            starCount: 0,
            title: "bestSeller product-08",
            price: "699.00",
            discount: 0,
            url: "#",
            bgImg: "https://source.unsplash.com/600x300/?furniture,shiny"
          },                                                                    
        ],                        
      },
      
      controller: "featuredCarousel",
      featured: true,
      latest: false,
      bestSeller: false,
    };
  },
  methods: {
    featuredShow(){
      this.featured = true;
      this.latest = false;
      this.bestSeller = false;
      this.controller = "featuredCarousel";
    },
    latestShow(){
      this.featured = false;
      this.latest = true;
      this.bestSeller = false;
      this.controller = "latestCarousel";
    },
    bestSellerShow(){
      this.featured = false;
      this.latest = false;
      this.bestSeller = true;
      this.controller = "bestSellerCarousel";
    },
  },
  mounted(){
    let featuredTarget = document.querySelector('.featuredProductsMobile .carousel-item');
    let latestTarget = document.querySelector('.latestProductsMobile .carousel-item');
    let bestSellerTarget = document.querySelector('.bestSellerProductsMobile .carousel-item');

    featuredTarget.classList.add('active');
    latestTarget.classList.add('active');
    bestSellerTarget.classList.add('active');
  },
}
</script>

<style lang="less" scope>
  @import '@/less/main.less';

  #carouselProducts, #carouselProductsMobile {
    padding-top: 1.5rem;
    .controller {
      padding: 0;
      padding-bottom: 1.5rem;
      .filter-title {
        padding: 0;
        span {
          font-size: 16px;
          font-weight: 700;
          color: #838182;
          text-transform: uppercase;
          cursor: pointer;
          &:nth-child(1) {
            padding-right: 15px;
          }
          &:nth-child(2) {
            padding: 0 15px;
            border-left: 1px solid #a8a8a8;
            border-right: 1px solid #a8a8a8;
          }
          &:nth-child(3) {
            padding-left: 15px;
          }
          &.active {
            color: #3a3a3a;
          }                  
        }
      }
      .controller-box {
        text-align: right;
        .box {
          display: flex;
          justify-content: space-around;
          align-items: center;
          margin-left: auto;
          width: 80px;
          border-radius: 20px;
          padding: 5px;
          background: #eee;
          .prev, .next {
            width: 30px;
            height: 30px;
            line-height: 29px;
            border-radius: 50%;
            text-align: center;
            background: #fff;
            color: @main-gray;
          }
        }
      }
    }
    // 低於576px將控制列隱藏，將filter-title置中顯示，user使用手指左右滑動瀏覽產品
    @media (max-width: 576px) {
      .controller {
        .filter-title {
          display: flex;
          justify-content: center;
          align-items: center;
        }
        .controller-box {
          display: none;
        }
      }
    }
    .items {
      padding: 0;
      .item {
        min-height: 260px;
      }
      .box {
        .imgBox {
          position: relative;
          width: 100%;
          height: 217px;
          overflow: hidden;
          .quick-action-box {
            position: absolute;
            margin: 0;
            width: 100%;
            height: 40px;
            bottom: 0;
            left: 0;
            transform: translateY(110%);
            transition: .3s all ease-in-out;
            .add-to-cart, .add-to-favorite {
              display: flex;
              align-items: center;
              justify-content: center;
              height: 100%;
              text-align: center;
              font-size: 14px;
              border: 1px solid #eee;
              background: #fff;
              color: #8a8a8a;
            }
          }
        }
        img {
          position: relative;
          left: -50%;
          height: 100%;
          width: auto
        }
        .info {
          padding: 0 5%;
          .star-count {
            svg {
              margin: 0 1px;
              width: 0.7rem;
              color: #c8a760;
            }
            &.hide {
              opacity: 0;
            }
          }
          .title {
            font-size: 15px;
            font-weight: 500;
            color: #747474;
          }
          .price {
            font-size: 19px;
            font-weight: 700;
            color: #333;
          }
        }
        &:hover {
          .quick-action-box {
            transform: translateY(0%);
          }
        }
      }
    }
  }
  #carouselProductsMobile {
    .items {
      .box {
        .imgBox {
          display: flex;
          justify-content: center;
          height: 290px;
          overflow: hidden;
          .quick-action-box {
            height: 30px;
            transform: translateY(0);
          }
          img {
            position: relative;
            left: 0;
            width: auto;
            height: 100%;
          }
        }
        @media (max-width: 992px) {
          .item {
            min-height: 280px;
            padding: 0 8px;
          }
          .imgBox {
            img {
              width: 100%;
            }
          }          
        }
        @media (max-width: 767px) {
          .imgBox {
            img {
              width: auto;
            }
          }     
        }       
      }    
    }
  }
</style>
