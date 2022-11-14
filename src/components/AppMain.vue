<script>
import CharactersList from './CharactersList.vue';

export default {
    name: "AppMain",
    components: { CharactersList }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="found_char">
                <h3>Found 62 characters</h3>
            </div>
            <CharactersList />
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.found_char {
    background-color: $bb-dark;

    h3 {
        color: $bb-light;
        padding: 1rem;
    }
}
</style>