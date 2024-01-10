<template>
  <div class="text-center py-8 title">
    <h1 class="">
      {{ title }}
    </h1>

    <p class="me-1 pt-3">{{ subtitle }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    subtitle: {
      type: String,
    },
  },
};
</script>
<style scoped lang="scss">
.title {
    h1{
        font-size: 45px;
    }
  p {
    color: #666666;
    font-size: 18px;
  }
}
</style>
