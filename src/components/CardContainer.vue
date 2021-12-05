<template>
  <div>
    <h2>Nuestros Platos</h2>
    <v-row>
      <v-col v-for="(product, i) in products" :key="i">
        <CardProduct
          :product="product"
          @AgregarAlCarrito="AgregarAlCarrito($event)"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import CardProduct from "./CardProducts.vue";

export default {
  props: {
    products: Array
  },
  components: {
    CardProduct
  },
  methods: {
    AgregarAlCarrito(pizza) {
      this.$emit("AgregarAlCarritoCardContainer", pizza);
    }
  }
};
</script>

<style scoped></style>
