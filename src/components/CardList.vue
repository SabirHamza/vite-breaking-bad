<script>
import CaracterCard from './CaracterCard.vue'
import { store } from '../data/store'


export default {
    data() {
        return {
            store
        }
    },

    components: { CaracterCard }
}

</script>

<template>
    <div v-for="caracter in store.caracters">
        <CaracterCard :img="caracter.card_images[0].image_url" :name="caracter.name" :type="caracter.archetype" />
    </div>
</template>

<style scoped></style>