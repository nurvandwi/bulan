<template>
  <div class="container">
    <Header title="Rebate" />
    <Cart :contentFor="'RebateDetails'" class="pt-4" />
    <Item :contentFor="'RebateDetails'" />
    <DetailPengiriman :contentFor="'RebateDetails'" />
    <FooterProduct :contentFor="'RebateDetails'" />
  </div>
</template>

<script>
import DetailPengiriman from "@/components/Catalog/DetailPengiriman.vue";
import Item from "@/components/Catalog/ListItem.vue";
import Cart from "@/components/Catalog/AlertCart.vue";
import Header from "@/components/Catalog/Header.vue";
import FooterProduct from "@/components/Catalog/FooterProduct.vue";
export default {
  components: {
    Header,
    Item,
    DetailPengiriman,
    Cart,
    FooterProduct
  }
};
</script>

<style scoped></style>
