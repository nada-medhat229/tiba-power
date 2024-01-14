<template>
<section class="mt-10 pt-10 ">
        <v-row class="mt-10">
            <v-col cols="12" md="5" class="text-center">
                <img :src="Groupmob" alt="" class="mobimg" width="90%"/>
                    <img :src="aboutimage" alt="" class="general" width="90%">
            </v-col>
            <v-col cols="12" md="5">
                <div class=" sectionabout ma-lg-10 ma-0 mr-lg-0  ">
    <h1 class="">
        من نحن
    </h1>

    <p class="me-1 pt-3">هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
        هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.

</p>
  </div>
            </v-col>
        </v-row>
        <v-container>
            <v-row class="mt-10">
          
            <v-col cols="12" md="6">
                <div class=" sectionabout ma-lg-10 ma-0 mr-lg-0 ">
    <h1 class="">
        من نحن
    </h1>

    <p class="me-1 pt-3">هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
        هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النص العربى، حيث يمكنك أن تولد مثل هذا النص أو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.

</p>
  </div>
            </v-col>
            <v-col cols="12" md="6">
                    <img :src="Groupsec" alt="" class="imggroupp" width="90%">
            </v-col>
        </v-row>
        </v-container>
       
</section>
</template>
<script>
import aboutimage from "../../assets/image/Groupppp.png"
import Groupmob from "../../assets/image/Groupmob.png"
import Groupsec from "../../assets/image/Groupsec.png"
export default {
    data() {
        return {
            aboutimage,
            Groupsec,
            Groupmob
        }
    },
    components:{
        
    }
}
</script>
<style lang="scss" scoped>
.imggroupp{
    margin-top: -70px;
}
.mobimg{
    display: none;
}
.general{
    display: inline;
}
    .sectionabout {
    h1{
        font-size: 45px;
    }
  p {
    font-size: 18px;
  }
}
@media (max-width: 960px) {
    .imggroupp{
    margin-top: 0;
}
    .sectionabout{
        width: 85%;
        margin: auto !important;
    }
    .mobimg{
        width: 50vw !important;
        margin: auto;
    display: inline-block;
}
.general{
    display: none;
}
}
</style>