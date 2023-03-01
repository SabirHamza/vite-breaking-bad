<script>
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
    }
}

</script>

<template>
    <div v-for="caracter in caracters" class="col-2">
        <img :src="caracter.card_images[0].image_url" class="img-fluid" alt="">
        <p>{{ caracter.name }}</p>
    </div>
</template>

<style scoped></style>