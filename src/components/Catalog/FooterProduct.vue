<template>
  <div class="container">
    <nav
      v-if="$route.name != 'categories' && $route.name != 'ewallet'"
      class="navbar-Container mx-auto mb-4 margin-desktop navbar navbar-expand navbar-dark backtheme footerstyle col-md-8 col-10 col-sm-10 col-lg-5"
    >
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'product'"
      >
        <router-link v-bind:to="'/productdetail'">
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16 border-right">
                  {{ cartItemCount }} Items
                </h5>
              </div>
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16">{{ cartTotalPrice }} Poin</h5>
              </div>

              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-cart.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>

      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'ewallet'"
      >
        <router-link v-bind:to="'/ewallet'">
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16 border-right">
                  {{ cartEwalletCount }} Items
                </h5>
              </div>
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16">
                  {{ cartEwalletPrice }} Poin
                </h5>
              </div>

              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-cart.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>

      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'PoinCash'"
      >
        <router-link v-bind:to="'/pointcashdetails'">
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16 border-right">
                  {{ cartPoincashCount }} Items
                </h5>
              </div>
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16">
                  {{ cartPoincashPrice }} Poin
                </h5>
              </div>

              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-cart.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>

      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'Rebate'"
      >
        <router-link v-bind:to="'/rebatedetails'">
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16 border-right">
                  {{ cartRebateCount }} Items
                </h5>
              </div>
              <div class="col-md-5 col-5">
                <h5 class="text-white m-0 font16">
                  {{ cartRebatePrice }} Poin
                </h5>
              </div>

              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-cart.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>

      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'RebateDetails'"
      >
        <router-link
          v-bind:to="'/SuccessPage'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-10 col-10">
                <h5 class="text-white m-0 font16">Checkout</h5>
              </div>
              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-next.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'EwalletDetails'"
      >
        <router-link
          v-bind:to="'/SuccessPage'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-10 col-10">
                <h5 class="text-white m-0 font16">Checkout</h5>
              </div>
              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-next.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'PointCashDetails'"
      >
        <router-link
          v-bind:to="'/SuccessPage'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-10 col-10">
                <h5 class="text-white m-0 font16">Checkout</h5>
              </div>
              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-next.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'ProductDetails'"
      >
        <router-link
          v-bind:to="'/SuccessPage'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-10 col-10">
                <h5 class="text-white m-0 font16">Checkout</h5>
              </div>
              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-next.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'PulsaDetails'"
      >
        <router-link
          v-bind:to="'/SuccessPage'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-10 col-10">
                <h5 class="text-white m-0 font16">Checkout</h5>
              </div>
              <div class="col-md-2 col-2">
                <img
                  src="../../assets/icon-next.png"
                  class="mr-5 img-cart"
                  alt
                />
              </div>
            </div>
          </div>
        </router-link>
      </div>
      <div
        class="container justify-content-center py-2"
        v-if="contentFor === 'Success'"
      >
        <router-link
          v-bind:to="'/Categories'"
          style="color: #FFF;"
          class="mx-auto font18"
        >
          <div class="nav navbar-nav">
            <div class="d-flex align-items-center">
              <div class="col-md-12 col-12">
                <h5 class="text-white m-0">Home</h5>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  props: ["contentFor"],
  computed: {
    cartItemCount() {
      return this.$store.getters.cartItemCount;
    },
    cartTotalPrice() {
      return this.$store.getters.cartTotalPrice;
    },
    cartEwalletCount() {
      return this.$store.getters.cartEwalletCount;
    },
    cartEwalletPrice() {
      return this.$store.getters.cartEwalletPrice;
    },
    cartPoincashCount() {
      return this.$store.getters.cartPoincashCount;
    },
    cartRebateCount() {
      return this.$store.getters.cartRebateCount;
    },
    cartPoincashPrice() {
      return this.$store.getters.cartPoincashPrice;
    },
    cartRebatePrice() {
      return this.$store.getters.cartRebatePrice;
    },
  },
};
</script>

<style scoped>
.backtheme {
  background: #4e37b2;
  border-radius: 100px;
}
.footerstyle {
  position: fixed !important;
  bottom: 0 !important;
  left: 0;
  right: 0;
  max-width: auto;
  z-index: 1030 !important;
}

@media screen and (max-width: 1000px) {
  .backtheme {
    background: #4e37b2;
    border-radius: 100px;
  }
  .font16 {
    font-size: 16px !important;
  }

  .img-cart {
    width: 30px;
    height: 30px;
  }
  @media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (orientation: portrait) {
    .footerstyle {
      position: fixed !important;
      bottom: 0 !important;
      left: 0;
      right: 0;
      min-height: 70px;
      max-width: 100vw;
      z-index: 1030 !important;
    }
  }
}
</style>
