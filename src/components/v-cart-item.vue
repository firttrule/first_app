<template>
  <div class="v-cart-item"></div>
</template>

<script>
export default {
  name: "v-cart-item",
  components: {},
  props: {},
  data() {
    return {};
  },
};
</script>

<style>
.v-cart-item {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 grey;
  padding: 20px;
  margin: 20px;
}
</style>
