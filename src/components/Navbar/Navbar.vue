<!-- eslint-disable vue/multi-word-component-names -->
<template>
   
    <div class="position-relative">
    <div class="naav">
      <v-row justify="space-between" align="center">
        <v-col cols="4" md="4"  class="py-sm-4 pb-0 pt-4">
          <img :src="logo" alt="" @click="redirectto('/')" />
        </v-col>
        <v-col cols="8" md="8" >
          <div class="navitem">
            <v-btn
              v-for="(item, index) in items"
              :key="index"
              @click="redirectto(item.route)"
              :ripple="false"
              variant="text"
              class="mx-md-2 mx-0 px-1 links"
              rounded="xl"
            >
              {{ item.text }}
            </v-btn>
          </div>
          <div
            id="mySidebar"
            :class="[style ? 'showing' : 'hiding', 'w3-sidebar']"
          >
            <div class="p-3">
              <div class="w-100 text-end">
                <v-icon @click="close()" icon="mdi-close"> </v-icon>
              </div>
              <v-list class="">
                <v-list-item
                  v-for="(item, index) in items"
                  :key="index"
                  @click="redirectto(item.route)"
                >
                  <v-list-item-title>{{ item.text }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </div>
          </div>

          <v-icon icon="mdi-menu" class="icon-menu mr-auto" @click="open()"></v-icon>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
import image from "../../../src/assets/image/logo.png";
export default {
  data: () => ({
    style: false,
    checksboxes: true,
    copunstype: true,
    copunsorder: true,
    copunsview: true,

    logo: image,
    dropdownOpen: false,
    items: [
      { text: "الرئيسية", route: "/" },
      { text: "خدماتنا", route: "/services" },
      { text: "منتجاتنا", route: "/products" },
      { text: " من نحن", route: "/about" },
      { text: " اتصل بنا", route: "/contact" },
    ],
  }),

  methods: {
    open() {
      this.style = !this.style;
    },

    close() {
      this.style = !this.style;
    },

    redirectto(path) {
      this.$router.push(path);
    },
    openDropdown() {
      this.dropdownOpen = true;
    },
    closeDropdown() {
      this.dropdownOpen = false;
    },
  },
};
</script>
<style scoped>
.icon-menu {
  display: none;
}

.hiding {
  display: none;
}
.w3-sidebar {
  height: 100%;
  width: 280px;
  background-color: #fff;
  position: fixed !important;
  z-index: 1111;
  overflow: auto;
  left: 0;
  top: 0;
  box-shadow: 12px 5px 40px 6px rgba(70, 87, 147, 0.08);
}

.naav {
  position: absolute;
  z-index: 1111;
  width: 80%;
  text-align: center;
}
.links {
  color: #616160;
  font-size: 18px;
  font-weight: 700;
}
.iconspan {
  cursor: pointer;
}
.iconspan span {
  color: #8b96a5 !important ;
}
@media (max-width: 1199.98px) {
  .naav {
    width: 90%;
  }
}
@media (max-width: 991.98px) {
}

@media (max-width: 767.98px) {
  .showing {
    display: block;
  }
  .icon-menu {
    display: block;
  }

  .navitem {
    display: none !important;
  }
}
@media (max-width: 575.98px) {
}
</style>
