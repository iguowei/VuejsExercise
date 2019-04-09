<template>
  <div>
    name: {{name}}
    <br/>
    type: {{type}}
    <br/>
    list: {{list}}
    <br/>
    isVisible: {{isVisible}}
    <br/>
    <button v-on:click="handleClick" v-bind:aa="$attrs['aa']">change type</button>
  </div>
</template>


<script>
export default {
    name: "PropsDemo",
    inheritAttrs: false,
    props: ["name", "type", "list", "isVisible", "onChange"],
    methods:{
        handleClick: function(){
            //this.type = "warning";

            this.onChange(this.type == "success" ? "warning": "success");
        }
    }
};
</script>

<style>
</style>

