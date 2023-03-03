<script>
import { store } from '../data/store'

export default {
    data() {
        return {
            store
        }
    },

    emits: ["selecttype"]
}
</script>

<template>
    <div class="container">
        <select class="form-select form-select-lg mb-3" aria-label=".form-select-lg example">
            <option v-for="type, index in store.types" :value="index">
                {{ store.types[index] }}
            </option>
        </select>
    </div>
</template>

<style></style>