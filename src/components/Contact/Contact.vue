<template>
  <section>
    <v-container>
      <v-card class="pa-md-5 pa-1 mx-md-16 mx-2">
        <h3 class="text-center titlecontact">
          اتصل بنا
          <hr
            width="120"
            style="
              height: 2px;
              border: none;
              border-radius: 50px;
              background-color: #6ba540;
            "
            class="text-center ma-auto mt-2"
          />
        </h3>
        <v-row class="pa-md-5 pa-2 ma-md-5 ma-0">
          <v-col cols="12" md="6">
            <v-text-field
              label="الاسم"
              variant="outlined"
              v-model="formData.name"
            ></v-text-field>
            <v-text-field
              label="البريد الالكتروني"
              variant="outlined"
              v-model="formData.email"
            ></v-text-field>
            <v-text-field
              label="رقم الجوال "
              variant="outlined"
              v-model="formData.phone"
            ></v-text-field>
            <v-textarea
              label=" اكتب رسالتك هنا"
              auto-grow
              variant="outlined"
              rows="3"
              row-height="25"
              shaped
              v-model="formData.message"
            ></v-textarea>
            <div class="text-red my-2">
              {{ errormessage ? errormessage : "" }}
            </div>
            <v-btn class="w-100 btnaction text-white" @click="addcontact">
              ارسال
            </v-btn>
          </v-col>

          <v-col cols="12" md="6" class="overflow-hidden">
            <div
              class="text-end font-weight-medium mt-md-12 pt-md-12 pt-2 mt-2"
            >
              <p class="py-2">0546010105 - 0537454644</p>
              <p class="py-2">taibapower@gmail.com</p>
              <div class="py-2">
                <v-icon icon="mdi mdi-twitter" class="mx-1"></v-icon>
                <v-icon icon="mdi mdi-facebook" class="mx-1"></v-icon>
                <v-icon icon="mdi mdi-instagram" class="mx-1"></v-icon>
                <v-icon icon="mdi mdi-youtube" class="mx-1"></v-icon>
              </div>
            </div>
            <l-map style="height: 300px" :zoom="zoom" :center="center">
              <l-tile-layer :url="url"></l-tile-layer>
              <l-marker :lat-lng="markerLatLng"></l-marker>
            </l-map>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
    <div class="d-md-flex d-none justify-space-between align-center py-md-16">
      <img :src="pathin" width="150" />
      <img :src="pathcon" width="150" />
    </div>
    <v-snackbar v-model="showSnackbar" color="green">
      سيتم الرد عليكم ف اقرب وقت ممكن
      <template v-slot:action="{ attrs }">
        <v-btn color="pink" v-bind="attrs" @click="showSnackbar = false">
          Close
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>
<script>
import axios from "axios";
import { LMap, LTileLayer, LMarker } from "vue3-leaflet";
import "leaflet/dist/leaflet.css";
import pathin from "../../assets/image/pathcontact.png";
import pathcon from "../../assets/image/pathcon.png";
export default {
  components: {
    LMap,
    LTileLayer,
    LMarker,
    showSnackbar: false,
  },
  data() {
    return {
      pathcon,
      pathin,
      url: "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      zoom: 4,
      center: [19.974265, 45.938586],
      markerLatLng: [24.774265, 46.738586],
      errormessage: "",
      formData: {
        name: "",
        email: "",
        phone: "",
        message: "",
      },
    };
  },
  methods: {
    async addcontact() {
      let res = await axios
        .post(`sendMail/contact.php`, this.formData, {
          headers: {
            "Content-type": "application/x-www-form-urlencoded",
          },
        })
        .then((result) => {
          this.errormessage = "";
          if (result.data.status) {
            this.showSnackbar = true;
          }
        })
        .catch((err) => {
          this.errormessage = err.message;
        });
    },
  },
};
</script>
<style lang="scss">
.leaflet-container.leaflet-touch-drag.leaflet-touch-zoom {
  min-height: 175px !important;
}
.btnaction {
  background: #6ba540;
}
.titlecontact {
  color: #6ba540;
}
</style>
