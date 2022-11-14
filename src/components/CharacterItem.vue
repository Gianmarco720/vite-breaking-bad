<script>
export default {
    name: 'CharacterItem',
    props: {
        character: Object
    }
}
</script>

<template>
    <div class="col">
        <div class="card">
            <img class="card-img-top" :src="character.img" :alt="character.name">
            <div class="card-body">
                <h4 class="card-title">{{ character.name }}</h4>
                <p class="card-text">{{ character.category }}</p>
                <p class="card-text">{{ character.status }}</p>
            </div>
        </div>
    </div>
</template>