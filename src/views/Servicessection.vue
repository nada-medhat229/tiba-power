<template>
  <section>
    <HeaderTitle
      title="خدماتنا"
      subtitle="يمكنكم الاطلاع علي جميع خدماتنا الآن"
    ></HeaderTitle>
    <v-container>
      <v-window
        v-model="window"
        class="elevation-0 position-relative pa-12 px-sm-12 px-3"
        :show-arrows="false"
      >
        <v-window-item v-for="(group, i) in groupeditems" :key="i">
          <v-row>
            <v-col cols="12" lg="4" v-for="(n, index) in group" :key="index">
              <Carditems
                :image="n.image"
                :title="n.title"
                :number="n.number"
              ></Carditems>
            </v-col>
          </v-row>
        </v-window-item>
        <div
          class="position-absolute d-flex justify-space-between arrow_card"
          style="top: -42px;left:0"
        >
          <v-btn icon @click="next" class="right_btn">
            <v-icon>
                mdi-arrow-right</v-icon>
          </v-btn>
          <v-btn icon @click="prev" class="left_btn">
            <v-icon>mdi-arrow-left</v-icon>
          </v-btn>
        </div>
      </v-window>
      <!-- <v-row>
        <v-col cols="12" md="4" v-for="(n,i) in items" :key="i">
            <Carditems
  :image="n.image"
  :title="n.title"
  :number="n.number"
  >
    </Carditems>
        </v-col>
    </v-row> -->
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
      window: 0,
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
  computed: {
    // Group the products into sub-arrays of 3
    groupeditems() {
      const groups = [];
      for (let i = 0; i < this.items.length; i += 3) {
        groups.push(this.items.slice(i, i + 3));
      }
      return groups;
    },
  },
  methods: {
    next() {
      this.window++;
      if (this.window >= this.groupeditems.length) {
        this.window = 0; // Wrap around to the first window
      }
    },
    prev() {
      this.window--;
      if (this.window < 0) {
        this.window = this.groupeditems.length - 1; // Wrap around to the last window
      }
    },
  },
};
</script>
<style lang="scss">
.arrow_card .v-btn--icon.v-btn--density-default {
    width: calc(var(--v-btn-height) + 1px);
    height: calc(var(--v-btn-height) + 1px);
}

.arrow_card .v-btn--icon.v-btn--size-default {
    --v-btn-size: .77rem;
    color: rgba(153, 153, 153, 0.5);
    border: 1px solid rgba(153, 153, 153, 0.5);
    box-shadow: none;
    margin: 0 5px;
}
.arrow_card .v-btn--icon:hover{
    color: white;
    background: rgba(107, 165, 64, 1);
    border: 1px solid rgba(107, 165, 64, 1);
}
</style>
