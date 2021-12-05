<template>
    <v-card class="pa-4">
        <h3>{{titulo}}</h3>
        <v-btn @click="enviarEventoPersonalizado()">Enviar</v-btn>
    </v-card>
</template>

<script>
    export default {
        props: {
            titulo: String
        },
        data() {
            return {
                mensajeSidebar: "Mensaje en sidebar"
            }
        },
        methods:{
            enviarEventoPersonalizado(){
                this.$emit("eventoNuevo", this.mensajeSidebar);
                console.log("entra al metodo");
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>