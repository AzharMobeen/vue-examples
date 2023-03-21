<template>
  <div class="homeDiv">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
  import HelloWorld from "@/components/HelloWorld";
  export default {
    name: `Home`,
    components: {
      HelloWorld
    }
  }
</script>
<style>
.homeDiv {
  background-color: aqua;
  height: 500px;
  text-align: center;
  align-content: center;
}
</style>