<script>
import CaracterCard from './CaracterCard.vue'

export default {

    props: { caracters: Array },

    components: { CaracterCard }
}

</script>

<template>
    <div v-for="caracter in caracters">
        <CaracterCard :img="caracter.card_images[0].image_url" :name="caracter.name" :type="caracter.archetype" />
    </div>
</template>

<style scoped></style>