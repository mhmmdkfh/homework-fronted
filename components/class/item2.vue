<template>
  <div class="card rounded-lg" style="width: 18rem;">
    <div>
      <div>
        <nuxt-link :to="'/class/'+id">
          <img :src="img" class="card-img-top" style="height: 100px; width: 100%;" alt="...">
        </nuxt-link>
      </div>
      <div>
        <nuxt-link :to="'/class/'+id">
          <h5 class="card-title">{{title}}</h5>
        </nuxt-link>
      </div>
      
    </div>
    
    <div class="card-body">
      
      <section v-if="homeworks.length">
        <h5>homework</h5>
        <ul>
          <li v-for="(homework,i) in homeworks" :key="i"> {{homework.title}}</li>
        </ul>
      </section>
    </div>
    <div class="card-footer text-muted">
      <slot name="footer"></slot>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    img: {
      type: String,
      default:
        "https://www.gstatic.com/classroom/themes/SocialStudies.jpg",
    },
    title: {
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
  },
};
</script>