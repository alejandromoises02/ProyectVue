<template>
    <v-card>
        <v-card-title>{{product.nombre}}</v-card-title>
        <v-card-text>
            <p>Precio: ${{product.precio}}</p>
            <img class="pizza" alt="pizza" :src="product.url">
            <v-btn @click="AgregarAlCarrito()">Agregar al carrito</v-btn>
        </v-card-text>
        
    </v-card>
</template>

<script>
    export default {
        props:{
            product : Object
        },
        methods:{
            AgregarAlCarrito(){
                this.$emit("AgregarAlCarrito", this.product);
            }
        }
    }
</script>

<style scoped>
.pizza{
  height: 100px;
}
</style>