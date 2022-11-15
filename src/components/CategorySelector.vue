<script>
import { store } from '../store.js';

export default {
    name: "CategorySelector",
    data() {
        return {
            categoryName: '',
        }
    }
}
</script>

<template>
    <main>
        <div class="filter">
            <select>
                <option value="breaking_bad">Breaking Bad</option>
                <option value="better_call_saul">Better Call Saul</option>
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