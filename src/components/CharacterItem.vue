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
        <div class="card rounded-0">
            <img class="card-img-top img-fluid p-2" :src="character.img" :alt="character.name">
            <div class="card-body">
                <h4 class="card-title text-uppercase">{{ character.name }}</h4>
                <p class="card-text">{{ character.category }}</p>
                <p class="card-text">{{ character.status }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.card {
    background-color: $bb-primary;
    height: 100%;

    h4 {
        color: $bb-light;
        text-align: center;
    }

    p {
        color: #606063;
        text-align: center;
        margin: 0;
    }
}
</style>