<template>
  <v-form v-model="valid" class="login">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="4"
          >
            <v-text-field
              v-model="Email"
              label="Ingresa tu email"
              required
            ></v-text-field>
          </v-col>
  
          <v-col
            cols="12"
            md="4"
          >
            <v-text-field
              v-model="pass"
              :rules="pass"
              :counter="10"
              label="Conrtraseña"
              required
            ></v-text-field>
          </v-col>
        </v-row>
        <button>Ingresar</button>
      </v-container>
      
    </v-form>
</template>

<script>
  export default {
    data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 10 || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid',
    ],
  }),
  }
</script>

<style scoped>
.login{
margin-top: 80px;
}
</style>