<template>
  <div class="v-catalog-item">
    <img
      class="v-catalog-item__image"
      :src="require('../assets/images/' + product_data.image)"
      alt="image"
    />
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">{{ product_data.price }}</p>
    <p class="v-catalog-item__about">{{ product_data.about }}</p>
    <button class="v-catalog-item__add_to_cart_btn" @click="sendDataToParent">
      Add to Cart
    </button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  components: {},
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  data() {
    return {};
  },
  methods: {
    sendDataToParent() {
      this.$emit("sendDataToParent", this.product_data.article);
    },
  },
};
</script>

<style lang="scss">
.v-cart-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 grey;
  padding: 20px;
  margin: 20px;
  &__img {
    max-width: 100px;
  }
}
</style>