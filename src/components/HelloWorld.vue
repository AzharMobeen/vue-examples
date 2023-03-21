<template>
  <div>
    {{msg}}
    <br/>
    <v-btn  variant="flat" color="secondary" v-on:click="firstMethod()">Toggle Button</v-btn>
    <v-table class="main-table" v-if="show" theme="dark">
      <thead>
      <tr>
        <th class="text-left">
          Id
        </th>
        <th class="text-left">
          Name
        </th>
      </tr>
      </thead>
      <tr v-for="user in users" :key="user.id">
        <td class="text-left">{{user.id}}</td>
        <td class="text-left">{{user.name}}</td>
      </tr>
    </v-table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    firstMethod() {
      this.show = !this.show;
      console.log("first method called!")
    },
    secondMethod(param) {
      console.log("secondMethod called with param :: "+ param);
      this.show = !this.show;
    }
  },
  data() {
    return {
      show: false,
      users: [
        {id: 1, name: "Umaima"},
        {id: 2, name: "Zuhayr"},
        {id: 3, name: "Ali"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main-table {
  width: 80%;
}
</style>
