<script>
export default {
    props: {
        img: String,
        name: String,
        type: String,
    }
}
</script>

<template>
    <div class="col text-center px-2">
        <div class="cards rounded-3">
            <img :src="img" class="img-fluid rounded-3" alt="">
            <span class="fw-bold text-light">{{ name }}</span>
            <h6 class="fw-bold py-3">{{ type }} </h6>
        </div>
    </div>
</template>

<style scoped>
.cards {
    background-color: orange;
}
</style>
