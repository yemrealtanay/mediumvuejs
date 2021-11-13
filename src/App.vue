<template>
  <v-app class="grey lighten-4">
    <Navbar/>

    <v-main class="mx-15 mt-5">
      <router-view/>
    </v-main>

    <v-footer padless>
      <v-col
        class="text-center"
        cols="12"
      >
        © {{ new Date().getFullYear() }} — <strong>Biz bunu Yunus Emre Altanay'la Birlite Yaptık!</strong>
      </v-col>
    </v-footer>

  </v-app>
</template>

<script>
import Navbar from '@/components/NavBar'
export default {
  name: 'App',
  components: {
    Navbar
  },
  data: () => ({
    //
  }),
};
</script>