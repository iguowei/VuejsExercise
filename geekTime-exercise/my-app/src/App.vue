<template>
  <div id="app">
    {{msg}}
    <input type="text" v-model="list">
    <button v-on:click="todoList">添加</button>
    <ol>
      <gw3 v-for="item in items" v-bind:item="item" v-bind:key="item" aa="userCustomer">
        <template v-slot:itemz="itemProps">
          <span v-bind:style="{fontSize: '19px', color: itemProps.check? 'red': 'blue'}">{{item}}</span>
        </template>
      </gw3>
    </ol>
  </div>
</template>

<script>
import gw3 from "./components/TodoItem.vue";

export default {
  name: "app",
  data: function() {
    return {
      msg: "Hello Vuejs",
      list: "",
      items: []
    }
  },
  methods: {
    todoList: function() {
      console.log(123);
      this.items.push(this.list);
      this.list = "";
    }
  },
  components: {
    gw3,
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
