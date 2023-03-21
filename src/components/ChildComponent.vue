<template>
  <div>
    <h6 v-if="inputDataPlaceHolder==null">{{this.inputDataPlaceHolder}}</h6>
    <input type="text" placeholder="{{this.inputDataPlaceHolder}}" v-model="inputData"/>
    <v-btn v-on:click="passDataToParent">Child Button for passing data to parent</v-btn>
  </div>
</template>

<script>
  //let inputData = "";
  export default {
    name: "ChildComponent",
    props: {
      inputDataPlaceHolder: String
    },
    data() {
      return {
        inputData: null,

      }
    },
    methods: {
      passDataToParent() {
        console.log("update parent message! :: ", this.inputData)
        this.$emit('updateParent', this.inputData)
      }
    }
  }
</script>

<style>

</style>