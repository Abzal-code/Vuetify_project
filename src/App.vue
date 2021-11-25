<template>
  <v-app>

    <Appheader/>

    <v-main>
      <v-container>
        <router-view class="view"></router-view>
      </v-container>
    </v-main>

    
    <Appfooter/>
  </v-app>
</template>

<script>
import Appfooter from './components/Appfooter.vue'
import Appheader from './components/Appheader.vue'

export default {
  name: 'App',

  components: {
    Appheader,
    Appfooter,
  },

  data: () => ({
    //
  }),
};
</script>
