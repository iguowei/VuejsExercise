<template>
  <li class="item">
    <input type="checkbox" v-model="check">
    <slot name="itemz" v-bind="{check}"></slot>
  </li>
</template>


<script>
export default {
  props: ["item"],
  inheritAttrs: false,
  data: function() {
    return {
      a: 10,
      check: true,
    }
  }
};
</script>


<style scoped>
.item {
  color: red;
}
</style>
