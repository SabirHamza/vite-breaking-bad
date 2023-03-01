<script>
import MainApp from './components/MainApp.vue'
import axios from 'axios'

export default {
  data() {
    return {
      caracters: []
    }
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0")
      .then((response) => {
        console.log(response);

        this.caracters = response.data.data

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
  <MainApp :caracters="caracters" />
</template>

<style></style>
