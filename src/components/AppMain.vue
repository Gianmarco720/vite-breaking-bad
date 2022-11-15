<script>
import CharactersList from './CharactersList.vue';
import CategorySelector from './CategorySelector.vue';
import { store } from '../store.js';
import axios from 'axios';

export default {
    name: "AppMain",
    components: { CharactersList, CategorySelector },
    data() {
        return {
            store
        }
    },
    methods: {
        searchCategory() {
            console.log('Changing in', this.store.categoryName);
            console.log((this.store.categoryName));
            const categoryName = this.store.categoryName;
            const url = `${this.store.API_URL}?category=${categoryName}`;
            console.log(url);

            axios.get(url)
                .then(resp => {
                    this.store.characters = resp.data
                    console.log(resp);
                })
                .catch(err => {
                    console.log(err);
                })
        }
    },
    computed: {
        totalResults() {
            return this.store.characters.length
        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <CategorySelector @searchData="searchCategory" />
            <div class="found_char">
                <h3 v-if="store.characters != null">Found {{ totalResults }} characters</h3>
            </div>
            <CharactersList />
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

.found_char {
    background-color: $bb-dark;

    h3 {
        color: $bb-light;
        padding: 1rem;
    }
}
</style>