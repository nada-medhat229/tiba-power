<template>
     <section>
        <div class="position-relative">
    <v-img :src="headerimage" class="main-image">
      <img
        :src="sky"
        alt=""
        style="position: absolute; left: 7%; z-index: 0; width: 80%"
      />
      <v-row
        justify="center"
        align="center"
        class="position-absolute collection-header"
      >
        <v-col cols="12" md="5">
          <img :src="stork" alt="" width="100%" class="stork" />
        </v-col>
        <v-col cols="12" md="7">
          <div class="content">
            <h1 class="text-white text-md-h2 text-h4">
              شركة قدرات طيبة للصناعة
            </h1>
            <p class="paragraph-text  py-md-5 py-2">
              شركة ذات مسئولية محدودة تأسست عام 2005_تواصل رحلتنا نحو النجاح في
              القطاع التعديني في مادة البوزلان
            </p>
            <button class="more_than">معرفة المزبد</button>
          </div>
        </v-col>
      </v-row>
    </v-img>
  </div>
</section>

</template>

<script>
import sky from "../../assets/image/pngwing.png";
import ghhhh from "../../assets/image/ghhhh.png";
import headerimage from "../../assets/image/Rectangl.png";
export default {
  data() {
    return {
      stork: ghhhh,
      sky: sky,
      headerimage: headerimage,
    };
  },
};
</script>
<style lang="scss" >
.collection-header {
  bottom: 25%;
}
.paragraph-text {
  font-size: 28px;
  color: #fff;

  width: 75% !important;
}
.more_than {
  border: 1px solid #fff;
  color: #fff;
  padding: 10px 15px;
  border-radius: 25px;
  font-size: 18px;
}
@media (max-width: 1199px) {
  .collection-header {
    bottom: 15%;
  }
}
@media (max-width: 960px) {
  .naav {
    width: 100%;
  }
  .stork {
    display: none;
  }
  .content {
    padding-right: 15px;
  }
 
}
@media (max-width: 767px) {
.main-image .v-img__img--contain {
    object-fit: cover !important;
}
    .main-image {
    height: 120vh;
  }
  .paragraph-text {
  font-size: 22px;
  width: 95% !important;
}
}
@media (max-width: 575px) {
}
</style>
