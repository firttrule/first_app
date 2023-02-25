<template>
  <div class="v-cart">
    <h2>Im Cart!</h2>
    <vCartItem />
  </div>
</template>

<script>
import vCartItem from "./v-cart-item.vue";
export default {
  name: "v-cart",
  components: {
    vCartItem,
  },
  props: {},
  data() {
    return {};
  },
};
</script>

<style>
</style>
