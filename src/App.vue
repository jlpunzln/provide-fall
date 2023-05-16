<template>
  <div>
    <label>Name</label>
    <input v-model="val" />
    <FallButton @click="buttonClick"  :list="list"/>
    <Personal :name="name" :list="list" />
    <button @click="toSub">Send to Sub</button>
  </div>
</template>

<script>
import FallButton from "./components/Fall.vue";

export default {
  name: "App",
  components: {
    FallButton,
  },
  data() {
    return {
      name: 'Complete',
      val: '',
      list:[],
      desclist:[]
    };
  },
  methods: {
    buttonClick() {
      this.list.push(this.val)
    },
    toSub(){
      this.desclist.push(this.val)
    }
  },
  provide(){
    return {
      list: this.desclist
    }
  }
};
</script>