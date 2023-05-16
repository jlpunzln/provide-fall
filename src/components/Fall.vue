<template>
  <div>
    <div>This is for fall attribute check</div>
    <div><button @click="buttonClick" v-bind="$attrs">Add button</button></div>
    <div><p v-for="(lst, index) in list" :key="index">{{lst}}</p></div>
    <div>Sub Area</div>
    <SubComponent />
  </div>
</template>

<script>
import SubComponent from "./Sub.vue";
export default {
  name: "FallButton",
  components: {
    SubComponent,
  },
  inheritAttrs: false,
  props:["list"],
};
</script>
