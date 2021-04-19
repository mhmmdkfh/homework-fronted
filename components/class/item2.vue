<template>
  <div class="card rounded-lg" style="width: 18rem;">
    <div>
      <div>
        <nuxt-link :to="'/class/'+id" class="text-decoration-none">
          <img :src="img" class="card-img-top" style="height: 100px; width: 100%;" alt="...">
        </nuxt-link>
      </div>
      <div class="card-img-overlay">
        <nuxt-link :to="'/class/'+id" class="text-decoration-none">
          <h5 class="card-title headerClass">{{title}}</h5>
          <p class="card-title headerClass mt">{{title2}}</p>
          <p class="card-title headerClass">{{nameClass}}</p>
        </nuxt-link>
      </div>
    </div>
    <div class="card-body ">
      <section v-if="homeworks.length">
        <ul type="none" class="text-align-left">
          <li v-for="(homework,i) in homeworks" :key="i"> {{homework.title}}</li>
        </ul>
      </section>
    </div>
    <div class="card-footer text-muted">
      <slot name="footer">
        <i :class="icon1" class="iconImg"></i>
        <i :class="icon2" class="iconImg"></i>
      </slot>
    </div>
  </div>
</template>
<script>

export default {
  props: {
    img: {
      type: String,
      default:
        "",
    },
    title: {
      type: String,
      default: "",
    },
    title2: {
      type: String,
      default: "",
    },
    nameClass: {
      type: String,
      default: "",
    },
    id: {
      type: String,
      default: "0",
    },
    homeworks: {
      type: Array,
      default: () => [],
    },
    icon1: {
      type: String,
      default: "",
    },
    icon2: {
      type: String,
      default: "",
    },
  },
};
</script>