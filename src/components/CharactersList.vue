<script>
import CharacterItem from './CharacterItem.vue';
import { store } from '../store.js'
export default {
    name: 'CharactersList',
    components: {
        CharacterItem
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <section class="characters" v-if="!store.loading">
        <div class="container">
            <div class="row row-cols-1 row-cols-sm-3 row-cols-md-5 g-3">
                <CharacterItem :character="character" v-for="character in store.characters" />
            </div>
        </div>
    </section>
    <div class="loader d-flex justify-content-center align-items-center p-5" v-else>
        <h1 class="text-white">Loading...</h1>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.characters {
    background-color: $bb-light;
}
</style>