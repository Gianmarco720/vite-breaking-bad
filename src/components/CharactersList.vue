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
    <section class="characters">
        <div class="container">
            <div class="row row-cols-1 row-cols-sm-3 row-cols-md-5 g-3">
                <CharacterItem :character="character" v-for="character in store.characters" />
            </div>
        </div>
    </section>
</template>