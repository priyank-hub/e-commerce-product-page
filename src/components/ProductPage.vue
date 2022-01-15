<template>
  <div class="">
    <div class="">
      <nav-bar />
    </div>

    <div class="container my-4">
      <div class="row align-items-center justify-content-between">

        <div class="col-12 col-md-5 p-0 p-md-2">
          <div class="d-flex flex-column">
            <div class="col-12">
              <div class="">
                <b-img :src="mainImage" alt="" style="width: 100%" class="image"></b-img>
              </div>
            </div>

            <div class="col-12 d-none d-md-block my-4">
              <div class="row">
                <div class="col-3" v-for="(image, index) in images" :key="index">
                  <div class="thumbnail" @click="changeMainImage(image)">
                    <b-img :src="image" style="width: 100%" alt="" class="image" :class="mainImage === image ? 'active' : ''"></b-img>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <div class="col-12 col-md-6 text-left my-3">
          <div class="container">
            <div>
              <span style="font-size: 13px; letter-spacing: 1px; color: hsl(26, 100%, 55%); font-weight: 700">
                SNEAKER COMPANY
              </span>
            </div>

            <div class="mt-2 mb-4">
              <span style="font-size: 40px; font-weight: 900; color: black; line-height: 2.8rem">
                Fall Limited Edition Sneakers
              </span>
            </div>

            <div class="my-3">
              <span class="text-muted">
                These low-profile sneakers are your perfect casual wear companion.
                Featuring a durable rubber outer sole, they'll withstand everything the weather can offer.
              </span>
            </div>

            <div class="row">
              <div class="col-8 col-md-12 d-flex flex-row align-items-center">
                <div>
                  <span style="font-size: 24px; font-weight: 900">
                    $125.00
                  </span>
                </div>
                <div class="">
                  <span class="mx-3 discount px-2 py-1 rounded" style="font-weight: 900; font-size: 14px; color: hsl(26, 100%, 55%)">
                    50%
                  </span>
                </div>
              </div>

              <div class="col-4 col-md-12 my-1">
                <span class="" style="font-weight: 700; color: rgb(183, 183, 183); text-decoration: line-through;">
                  $250.00
                </span>
              </div>
            </div>

            <div class="my-3 row">
              <div class="col-12 col-md-4 text-center px-md-0 mt-3">
                <div class="bg-quantity d-flex flex-row justify-content-between" style="font-weight: 700">
                  <div class="plus-minus">
                    <i class="fas fa-minus" @click="decrement()"></i>
                  </div>
                  <div class="">
                    {{ count }}
                  </div>
                  <div class="plus-minus">
                    <i class="fas fa-plus" @click="increment()"></i>
                  </div>
                </div>
              </div>
              <div class="col-12 col-md-8 text-center mt-3">
                <div class="bg-add-cart">
                  <span class="mx-3">
                    <i class="fas fa-shopping-cart text-white"></i>
                  </span>
                  <span style="font-weight: 700">
                    Add to cart
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
import NavBar from './NavBar'

export default {
  name: 'ProductPage',
  props: {

  },
  components: {
    NavBar
  },
  data() {
    return {
      count: 0,
      mainImage: '/assets/image-product-1.jpg',
      images: [
        '/assets/image-product-1.jpg',
        '/assets/image-product-2.jpg',
        '/assets/image-product-3.jpg',
        '/assets/image-product-4.jpg'
      ],
    }
  },
  methods: {
    increment() {
      this.count += 1;
    },
    decrement() {
      if (this.count - 1 >= 0) {
        this.count -= 1;
      }
    },
    changeMainImage(image) {
      this.mainImage = image;
    }
  }
}
</script>
<style scoped>
.image {
  border-radius: 10px;
}

@media (max-width: 768px) {
  .image {
    border-radius: 0px !important;
  }
}

.discount {
  /* border-radius: 10px; */
  background-color: hsl(25, 100%, 94%);
}

.bg-quantity {
  background-color: #f1f1f1;
  border-radius: 10px;
  font-size: 16px;
  padding: 14px;
}

.bg-add-cart {
  background-color: hsl(26, 100%, 55%);
  color: white !important;
  border-radius: 10px;
  font-size: 15px;
  padding: 14px;
  transition: 0.3s;
  cursor: pointer;
}

.bg-add-cart:hover {
  background-color: hsl(24, 91%, 86%);
}

.plus-minus {
  color: hsl(26, 100%, 55%);
  cursor: pointer;
}

.thumbnail img{
  cursor: pointer;
  opacity: 1;
  transition: .3s;
}

.thumbnail:hover img{
  /* background-color: #d2d2d2 !important;  */
  opacity: 0.3 !important;
}

.active {
  opacity: 0.4 !important;
  border: 3px solid hsl(26, 100%, 55%) !important;
}

i {
  transition: 0.3s;
}

i:hover {
  color: hsl(24, 91%, 86%);
}
</style>