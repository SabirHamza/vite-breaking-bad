<script>
import axios from 'axios'
import { store } from './data/store'
import MainApp from './components/MainApp.vue'
import SelectApp from './components/SelectApp.vue'

export default {
  data() {
    return {
      store
    }
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((response) => {
        console.log(response);

        store.caracters = response.data.data
      })
  },

  methods: {
    changeapi(param1) {
      console.log(param1);
    }
  },

  components: { MainApp, SelectApp }

}
</script>

<template>
  <header>
    <div class="container">
      <h1>Yu-Gi-Oh App</h1>
    </div>
  </header>
  <SelectApp @searchtype="changeapi()" />
  <MainApp />
</template>

<style></style>
