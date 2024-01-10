<template>
  <v-card class="mx-auto carditem"  style="border-radius: 15px">
    <v-img
      class="align-end text-white"
      height="300"
      style="border-radius: 15px"
      :src="image"
      cover
    >
    </v-img>
<div class="py-5 text-black">
    <h4 > {{ title }} </h4>
    <span>
        {{ number }}
    </span>
</div>
 
  </v-card>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
    },
    title: {
      type: String,
    },
    number: {
      type: Number,
    },
  },
};
</script>
<style scoped lang="scss">
.carditem {
    text-align: center;
  box-shadow: 0px 4px 4px 0px #6ba540;
}
</style>
