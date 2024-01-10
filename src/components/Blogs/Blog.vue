<template>
  <section class="blog pb-md-16 pb-5">
    <HeaderTitle
      title="المدونة"
      subtitle="يمكمك متابعة احدث الأخبار والمقالات "
    ></HeaderTitle>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="4" sm="6"   v-for="(item, i) in items" :key="i">
          <div>
            <img :src="item.image" height="200" width="100%" class="img_blog"/>
            <p>
                {{ item.title }}
            </p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import serv1 from "@/assets/image/serv1.png";
import serv2 from "@/assets/image/serv2.png";
import serv3 from "@/assets/image/remal.png";
import HeaderTitle from "../HeaderTitle/HeaderTitle.vue";
export default {
  components: {
    HeaderTitle,
  },
  data() {
    return {
      items: [
        {
          image: serv1,
          title:
            "هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.",
        },
        {
          image: serv2,
          title:
            "هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.",
        },
        {
          image: serv3,
          title:
            "هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.blog{
    text-align: center;
    .img_blog{
        border-radius: 25px;
    }
    p{
        font-size: 18px;
        padding-top: 10px;
        line-height: 32px;
    }
}
</style>
