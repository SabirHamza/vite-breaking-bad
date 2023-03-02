<script>
import { store } from '../data/store'

export default {
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container">
        <select class="form-select form-select-lg mb-3" aria-label=".form-select-lg example">
            <option selected>Open this select menu</option>
            <option v-for="type, index in store.types">
                {{ store.types[index] }}
            </option>
        </select>
    </div>
</template>

<style></style>