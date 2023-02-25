<template>
  <h1>Hello Im Catalog!</h1>
  <div class="v-catalog">
    <vCatalogItem
      v-for="product in PRODUCTS"
      :key="product.article"
      :product_data="product"
      @sendDataToParent="showArticleFromChild"
    />
  </div>
</template>

<script>
import vCatalogItem from "./v-catalog-item.vue";
import { mapActions, mapGetters } from "vuex";

export default {
  name: "v-catalog",
  components: {
    vCatalogItem,
  },
  props: {},
  data() {
    return {};
  },
  computed: {
    ...mapGetters(["PRODUCTS"]),
  },
  methods: {
    ...mapActions(["GET_PRODUCTS_FROM_API"]),

    showArticleFromChild(data) {
      console.log(data);
    },
  },
  mounted() {
    this.GET_PRODUCTS_FROM_API().then((response) => {
      if (response.data) {
        console.log("Данные пришли");
      }
    });
  },
};
</script>

<style>
.v-catalog {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
}
</style>
