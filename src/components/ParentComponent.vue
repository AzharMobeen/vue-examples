<template>
  <div>
    <h3>{{parentHead}}</h3>
    <h6>{{childData}}</h6>

    <ChildComponent inputDataPlaceHolder="Please enter data here" v-on:updateParent="getDataFromChild($event)"/>
  </div>
</template>

<script>
  import ChildComponent from "@/components/ChildComponent";
  export default {
    name: 'ParentComponent',
    props: {
    },
    components: {
      ChildComponent
    },
    data() {
      return {
        parentHead: "Parent component",
        childData: ""
      }
    },
    methods: {
      getDataFromChild(data) {
        console.log("get data object from child :: ", data);
        this.childData = data;
      }
    }
  }
</script>