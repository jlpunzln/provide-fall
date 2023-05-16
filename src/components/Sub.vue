<template>
  <div>
    <p>I am Sub</p>
    <div><p v-for="(lst, index) in list" :key="index">{{lst}}</p></div>
  </div>
</template>

<script>
export default {
  name: "SubComponent",
  inject:["list"],
  data(){
    return {
      list: this.list
    }
  }
};
</script>
