<script>
import CardList from './CardList.vue';

export default {

    props: { caracters: Array },

    components: { CardList }
}
</script>

<template>
    <main class="py-4">
        <div class="container">
            <div class="counter fw-bold mx-2 py-2"> Found <span>{{ caracters.length }}</span> cards</div>
            <div class="row row-cols-5">
                <CardList :caracters="caracters" />
            </div>
        </div>
    </main>
</template>

<style scoped>
main {
    background-color: orange;
}

.container {
    background-color: white;
}

.counter {
    background-color: black;
    color: white;
}
</style>
