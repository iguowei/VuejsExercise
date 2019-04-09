<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <Props aa="aa1"
      name="Hello Vue！"
      :type="type"
      :is-visible="false"
      :on-change="handlePropChange"
      title="属性Demo"
      class="test1"
      :class="['test2']"
      :style="{ marginTop: '20px' }"
      style="margin-top: 10px"></Props>
  </div>
</template>

<script>
import Props from "./components/Props.vue";

export default {
  name: "app",
  data: function() {
    return {
      type: "success",
      name: "123"
    };
  },
  components: {
    Props
  },
  methods: {
    handlePropChange: function(val){
      this.type = val
    }
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
