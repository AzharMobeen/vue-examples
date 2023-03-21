<template>
  <div>
    <input type="text" v-model="loginForm.username" placeholder="Please enter username"/>
    <input type="password" v-model="loginForm.password" placeholder="Please enter password">
    <v-btn v-on:click="submitForm">Submit</v-btn>
  </div>
</template>

<script>
  export default {
    name: 'FormComponent',
    props: {

    },
    methods: {
      submitForm() {
        console.log('Submit form called! :: ', this.loginForm);
      }
    },
    data() {
      return {
        loginForm: {
          username: null,
          password: null
        }
      }
    }
  }
</script>

<style>

</style>