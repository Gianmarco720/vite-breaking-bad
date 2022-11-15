<script>
import CharactersList from './CharactersList.vue';
import CategorySelector from './CategorySelector.vue';

export default {
    name: "AppMain",
    components: { CharactersList, CategorySelector },
}
</script>

<template>
    <main>
        <div class="container">
            <CategorySelector />
            <div class="found_char">
                <h3>Found 62 characters</h3>
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