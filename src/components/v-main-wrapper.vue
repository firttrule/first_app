<template>
  <div class="v-main-wrapper">
      <router-view></router-view>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "v-main-wrapper",
  props: {},
  data() {
    return {
      title: "hello!",
    };
  },
  computed: {
    ...mapGetters(["CART"]),
  },
  methods: {},
  watch: {},
  mounted() {
    console.log("hello Im here!");
  },
};
</script>

<style>
.v-main-wrapper {
  max-width: 900px;
  margin: 0 auto;
}
</style>
