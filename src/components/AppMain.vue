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
            <div class="filter">
                <select>
                    <option value="breaking_bad">Breaking Bad</option>
                    <option value="better_call_saul">Better Call Saul</option>
                </select>
            </div>
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