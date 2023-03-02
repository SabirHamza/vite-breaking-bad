<script>
import axios from 'axios'
import { store } from './data/store'
import MainApp from './components/MainApp.vue'

export default {
  data() {
    return {
      store
    }
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0")
      .then((response) => {
        console.log(response);

        store.caracters = response.data.data

        console.log(this.caracters);
      })
  },

  components: { MainApp }

}
</script>

<template>
  <header>
    <div class="container">
      <h1>Yu-Gi-Oh App</h1>
    </div>
  </header>
  <MainApp />
</template>

<style></style>
