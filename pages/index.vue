<template>
  <div>
    <partials-title>PERTEMUAN SENIN</partials-title>
    <center>{{i}}</center>
    <center>{{getBookPublish}}</center>
    <atoms-float-button @click.native="increment"/>

  </div>
</template>
<script>
export default {
  data() {
    return {
      i: 0,
      books: ["vue 1", "vue 2", "vue 3"],
    };
  },
  computed:{
    getBookPublish(){
      return this.i>3 ? "yes" : "no";
    }
  },
  methods: {
    increment() {
      this.i++;
    },
  },
};
</script>