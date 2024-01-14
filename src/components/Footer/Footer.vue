<template >
   <section class="footergeneral">
    <v-container>
        <v-row>
            <v-col cols="12" sm="4">
                <img :src="logo" alt="" @click="redirectto('/')" />
                <p class="w-75 text-white">
                    شركة ذات مسئولية محدودة تأسست عام 2005_تواصل رحلتنا نحو النجاح في القطاع التعديني في مادة البوزلان
                </p>
                <div class="mt-4">
                    <img :src="linkedin" alt="" class="mx-2 social">
                    <img :src="facebook" alt="" class="mx-2 social">
                    <img :src="twitter" alt="" class="mx-2 social">
                </div>
            </v-col>
            <v-col cols="12" sm="1"></v-col>
            <v-col cols="12" sm="3" >
                <h3 class="text-white mt-sm-8 mt-0 mb-sm-5 mb-3">
                    عنا
                </h3>
                <p class="mb-3 text-white routepage"  v-for="(item, index) in items"
                  :key="index"
                  @click="redirectto(item.route)">
                  {{ item.text }}
                  </p>
            </v-col>
            <v-col cols="12" sm="4" >
                <h3 class="text-white mt-sm-8 mt-0 mb-sm-5 mb-3">
                    ابق علي معرفة بكل جديد
                </h3>
                <p class="mb-3 text-white routepage"
                 >
                 انضم الينا لمعرفة اخبارنا وكل ما هو جديد ومميز من منتجاتنا
                  </p>
            </v-col>
        </v-row>
    </v-container>
   </section>
</template>
<script>
import image from "../../../src/assets/image/logo.png";
import linkedin from "../../../src/assets/image/linkedin.png";
import facebook from "../../../src/assets/image/facebook.png";
import twitter from "../../../src/assets/image/twitter.png";
export default {
    data(){
        return{
            logo: image,
            linkedin,
            facebook,
            twitter,
            items: [
      { text: "خدماتنا", route: "/services" },
      { text: "منتجاتنا", route: "/products" },
      { text: " من نحن", route: "/about" },
      { text: " اتصل بنا", route: "/contact" },
    ],
        }
    },
    methods:{
        redirectto(path) {
      this.$router.push(path);
    },
    }
}
</script>
<style lang="scss">
    .footergeneral{
        background: linear-gradient(212deg, #87876F 19.24%, #6BA540 136.13%);
    .routepage{
        font-size: 20px;
    }
    }
    .social{
        width: 30px;
    }
</style>