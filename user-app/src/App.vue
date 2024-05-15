<template>
  <v-app>
    <HeaderSideBar/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HeaderSideBar from './components/Header-SideBar.vue';
export default defineComponent({
  name: 'App',
  components:{
    HeaderSideBar
  },
  data () {
    return {
      //
    }
  },
})
</script>
