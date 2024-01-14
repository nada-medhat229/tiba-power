<template>
  <v-app>
    <v-main>
      <div v-if="$route.path == '/'">
        <Navbar />
      </div>
      <div v-else>
        <Navbar class="item" />
      </div>
      <router-view/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar/Navbar.vue"
import Footer from "./components/Footer/Footer.vue"
export default {
  name: 'App',
  components:{
    Navbar,
    Footer
  },
  data: () => ({
    //
  }),
}
</script>
<style lang="scss">
.item .naav{
background: #fff;
position: relative;
margin-bottom: 15px;
margin-top: 15px;
}
</style>