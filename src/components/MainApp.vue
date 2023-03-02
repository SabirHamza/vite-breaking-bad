<script>
import CardList from './CardList.vue';
import { store } from '../data/store'

export default {
    data() {
        return {
            store
        }
    },

    components: { CardList }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="counter fw-bold m-2 p-2 rounded-2"> Found <span>{{ store.caracters.length }}</span> cards</div>
            <div class="row row-cols-5">
                <CardList />
            </div>
        </div>
    </main>
</template>

<style scoped>
.counter {
    background-color: black;
    color: white;
}
</style>
