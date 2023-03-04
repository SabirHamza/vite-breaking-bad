<script>
import { store } from '../data/store'

export default {
    data() {
        return {
            store,
            selecttype: ""
        }
    },

    emits: ["searchtype"],

    methods: {
        selectedtype() {
            this.$emit('searchtype', this.selecttype)
        }
    }

}
</script>

<template>
    <div class="container">
        <select v-model="selecttype" @change="selectedtype()" class="form-select form-select-lg mb-3"
            aria-label=".form-select-lg example">
            <option v-for="type, index in store.types">
                {{ store.types[index] }}
            </option>
        </select>
    </div>
</template>

<style></style>