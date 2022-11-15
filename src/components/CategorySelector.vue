<script>
import { store } from '../store.js';

export default {
    name: "CategorySelector",
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <main>
        <div class="filter">
            <select v-model="store.categoryName" @change="$emit('searchData')">
                <option value="" disabled selected hidden>Choose a category</option>
                <option value="Breaking Bad">Breaking Bad</option>
                <option value="Better Call Saul">Better Call Saul</option>
            </select>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.filter {
    select {
        padding: 0.75rem;
        margin-bottom: 1rem;
        border-radius: 0.25rem;
    }
}
</style>