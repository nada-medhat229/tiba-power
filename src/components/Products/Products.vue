<template>
  <section>
    <HeaderTitle
      title="منتجاتنا"
      subtitle="يمكنكم الاطلاع علي جميع منتجاتنا الآن"
    ></HeaderTitle>
    <section class="position-relative main">
      <img :src="patii" alt="" class="w-100" style="margin-top: -22%" />

      <div class="sectionpro">
        <div>
          <h1>اسم المنتج</h1>

          <p class="me-1 pt-3 w-75">
            هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا
            النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد
            من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
          </p>
        </div>
        <v-img :src="Groupimg" class="mainimage">
          <img :src="pngwingtr" alt="" class="ma-md-auto ma-0" width="80%" />
        </v-img>
        <div class="replace text-center">
          <img :src="rep" alt="" class="ma-auto" width="60%"/>
        </div>
      </div>

      <div class="sectionpro sec">
        <v-img :src="Groupimg" class="mainimage">
          <img :src="rrmmm" alt="" class="ma-md-auto ma-0" width="80%" />
        </v-img>
        <div class="replace text-center">
          <img :src="repl" alt="" class="ma-auto" width="60%"/>
        </div>
        <div>
          <h1 class="w-75 mr-auto">اسم المنتج</h1>

          <p class="me-1 pt-3 w-75 mr-auto">
            هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا
            النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد
            من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
          </p>
        </div>
      </div>
    </section>
    <section class="position-relative main">
      <img :src="patii" alt="" class="w-100" style="margin-top: -22%" />

      <div class="sectionpro">
        <div>
          <h1>اسم المنتج</h1>

          <p class="me-1 pt-3 w-75">
            هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا
            النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد
            من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
          </p>
        </div>
        <v-img :src="Groupimg" class="mainimage">
          <img :src="pngwingtr" alt="" class="ma-md-auto ma-0" width="80%" />
        </v-img>
        <div class="replace text-center">
          <img :src="rep" alt="" class="ma-auto" width="60%"/>
        </div>
      </div>

      <div class="sectionpro sec">
        <v-img :src="Groupimg" class="mainimage">
          <img :src="rrmmm" alt="" class="ma-md-auto ma-0" width="80%" />
        </v-img>
        <div class="replace text-center">
          <img :src="repl" alt="" class="ma-auto" width="60%"/>
        </div>
        <div>
          <h1 class="w-75 mr-auto">اسم المنتج</h1>

          <p class="me-1 pt-3 w-75 mr-auto">
            هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا
            النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد
            من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
          </p>
        </div>
      </div>
    </section>
  </section>
</template>
<script>
import rep from "@/assets/image/replace.png"
import repl from "@/assets/image/rep.png"
import HeaderTitle from "@/components/HeaderTitle/HeaderTitle.vue";
import patii from "@/assets/image/Patii.png";
import Groupimg from "@/assets/image/Groupimg.png";
import pngwingtr from "@/assets/image/pngwingtr.png";
import rrmmm from "@/assets/image/rrrmm.png";
export default {
  components: {
    HeaderTitle,
  },
  data() {
    return {
      patii,
      Groupimg,
      pngwingtr,
      rrmmm,
      rep,
      repl
    };
  },
};
</script>
<style lang="scss">
.mainimage .v-responsive__content {
  display: flex !important;
}
</style>
<style lang="scss" scoped>
.replace{
  display: none;
}
.mainimage {
  width: 280px;
}
.sectionpro {
  margin-bottom: 70px;
  display: flex;
  position: absolute;
  width: 70%;
  right: 20%;
  top: 10%;
  justify-content: center;
  align-items: center;
  h1 {
    font-size: 36px;
  }
  p {
    font-size: 18px;
  }
}
.sectionpro.sec {
  top: 50%;
  bottom: 0%;
}
@media (max-width: 1199.98px) {
  .sectionpro {
    right: 5%;
    width: 90%;
  }
  
}
@media (max-width: 991.98px) {
  .mainimage {
    width: 200px;
  }
}
@media (max-width: 767.98px) {
  .mainimage {
display: none;  }
.replace{
  display: inline;
}
  .sectionpro {
    top: 0;
    flex-direction: column;
    p {
      width: 95% !important;
    }
  }
  .sectionpro.sec {
    top: 2%;
    h1{
        margin-right: 0 !important;
    }
    p{
        margin-right: 0 !important;
    }
  }
  .main{
    height: 280vh;
  }
  .main >img{
   margin-top: 0 !important;
   transform: scale(1.8);
  }
}
@media (max-width: 575.98px) {
    .sectionpro.sec {
    top: 0%;}
}
</style>
