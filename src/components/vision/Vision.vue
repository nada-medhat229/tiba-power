<template>
  <section class="position-relative">
    <img
      :src="path"
      class="position-absolute imging"
      style="width: 63vw; top: -60px"
    />
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
          <Content />
        </v-col>
        <v-col cols="12" md="6">
          <Imagesside />
        </v-col>

      </v-row>
    </v-container>
  </section>
</template>
<script>
import path from "../../assets/image/Path.png";
import Content from "./Content.vue";
import Imagesside from "./Imagesside.vue";
export default {
  components: {
    Content,
    Imagesside,
  },
  data() {
    return {
      path: path,
    };
  },
};
</script>
<style lang="scss">
@media (max-width: 960px) {
  .imging {
    display: none;
  }
}
</style>
