<template>
  <v-app>
    <Navbar />
    <Login />
    <Register />

    <v-row class="mt-12">
      <v-col>
        <CardContainer
          :products="products"
          @AgregarAlCarritoCardContainer="AgregarAlCarritoCardContainer($event)"
        />
      </v-col>
    </v-row>
    <v-row class="mt-12">
      <v-col>
      <Carrito 
      :carrito="carrito"
      />
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
import products from "./assets/data/products.json";
import Navbar from "./components/Navbar.vue";
import Login from './components/Login.vue'
import Register from './components/Register.vue'
import CardContainer from "./components/CardContainer.vue";
import Carrito from "./components/Carrito.vue";
export default {
  components: {
    Navbar,
    //Sidebar,
    CardContainer,
    Carrito,
    Login,
    Register
  },
  data() {
    return {
      products,
      carrito: [],
    };
  },
  methods: {
    AgregarAlCarritoCardContainer(pizza) {
      this.carrito = [...this.carrito, pizza]
    }
  }
};
</script>

<style scoped></style>
