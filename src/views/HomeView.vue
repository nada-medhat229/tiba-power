<template>
  <section>
    <Header />
    <Servicessection />
    <Vision />
    <v-container>
      <v-row>
      <v-col cols="12">
            <div class="w-100 text-end">
                <img :src="Pattern" alt="" >
            </div>
        </v-col>
    </v-row>
    </v-container>
   
    <Blog />
  </section>
</template>

<script>
import { defineComponent } from "vue";

// Components
import Pattern from "../assets/image/Pattern.png";
import Header from "../components/Header/Header.vue";
import Vision from "../components/vision/Vision.vue";
import Blog from "../components/Blogs/Blog.vue";
import Servicessection from "./Servicessection.vue";

export default defineComponent({
  name: "HomeView",
  data() {
    return {
      
      Pattern,
    };
  },
  components: {
    Header,
    Servicessection,
    Vision,
    Blog,
  },
});
</script>
