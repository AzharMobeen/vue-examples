<template>
<!--  <img alt="Vue logo" src="./assets/logo.png">-->
  <Home/>
  <ParentComponent/>
  <FormComponent/>
</template>

<script>
import Home from './components/Home.vue'
import ParentComponent from "@/components/ParentComponent";
import FormComponent from "@/components/FormComponent";

export default {
  name: 'App',
  components: {
    Home,
    ParentComponent,
    FormComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
