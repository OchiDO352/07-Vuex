<template>
  <div class="container">
    <div class="row">
      <h1 class="card">CATALOG</h1>
      <div
        class="card border-dark"
        style="width: 20rem"
        v-for="item in products"
        :key="item.id"
      >
        <img :src="item.imgUrl" class="card-img-top" :alt="item.title" />
        <div class="card-body">
          <center>
            <p class="card-title">{{ item.title }}</p>
          </center>
          <center>
            <p class="card-text">{{ item.price.toLocaleString() }} บาท</p>
          </center>
          <br />
          <center>
            <button class="btn btn-dark" @click="addItemToCart(item)">
              หยิบใส่ตะกร้า
            </button>
          </center>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "Shop",
  mounted() {
    this.getProducts();
  },
  computed: {
    ...mapGetters(["products"]),
  },
  methods: {
    ...mapActions(["addItemToCart", "getProducts"]),
  },
};
</script>

<style scoped>
.card {
  padding: 20px;
  margin: 10px;
  border: none;
  font-family: "Prompt", sans-serif;
}
</style>
