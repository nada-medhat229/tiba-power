<template>
  <section class="mt-16 pt-16">
    <HeaderTitle
      title="خدماتنا"
      subtitle="يمكنكم الاطلاع علي جميع خدماتنا الآن"
    ></HeaderTitle>
    <v-container>
      <v-row class="pa-md-10 pa-5">
        <v-col cols="12" lg="4" v-for="(n, index) in items" :key="index" class="mb-md-10 mb-8" >
          <Carditems
            :image="n.image"
            :title="n.title"
            :number="n.number"
           
          ></Carditems>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import stork from "@/assets/image/Image.png";
import serv1 from "@/assets/image/serv1.png";
import serv2 from "@/assets/image/serv2.png";
import HeaderTitle from "@/components/HeaderTitle/HeaderTitle.vue";
import Carditems from "@/components/Carditems/Carditems.vue";
export default {
  components: {
    HeaderTitle,
    Carditems,
  },
  data() {
    return {
      items: [
        {
          image: stork,
          title: "البودرة البركانية",
          number: "0/3",
        },
        {
          image: serv1,
          title: "البودرة البركانية",
          number: "0/5",
        },
        {
          image: serv2,
          title: "البحص البركاني ",
          number: "3/8",
        },
        {
          image: stork,
          title: "البودرة البركانية",
          number: "0/3",
        },
        {
          image: serv1,
          title: "البودرة البركانية",
          number: "0/5",
        },
        {
          image: serv2,
          title: "البحص البركاني ",
          number: "3/8",
        },
      ],
    };
  },
};
</script>
<style lang="scss"></style>
