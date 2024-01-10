<template>
  <section>
    <Header />
    <Servicessection />
    <Vision />
    <Blog />
  </section>
</template>

<script>
import { defineComponent } from "vue";

// Components
import Header from "../components/Header/Header.vue";
import Vision from "../components/vision/Vision.vue";
import Blog from "../components/Blogs/Blog.vue";
import Servicessection from "./Servicessection.vue";

export default defineComponent({
  name: "HomeView",

  components: {
    Header,
    Servicessection,
    Vision,
    Blog,
  },
});
</script>
