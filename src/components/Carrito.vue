<template>
  <v-data-table
      :headers="Carritoheaders"
      :items="carrito"
      class="elevation-1"
      hide-default-footer
    >
  </v-data-table>
</template>

<script>
export default {
  props: {
    carrito: Array,
  },
  data() {
    return {
      Carritoheaders: [
        { text: "Nombre ", value: "nombre" },
        { text: "Precio", value: "precio" },
      ],
    };
  },
};
</script>

<style scoped>
</style>