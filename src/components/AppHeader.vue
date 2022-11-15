<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <div class="logo d-flex align-items-center p-4">
            <img src="../assets/img/breaking_bad.png" alt="">
            <h1>Breaking Bad Api</h1>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.logo {
    img {
        width: 100px;
    }

    h1 {
        color: $bb-light;
        padding: 1rem;
    }
}
</style>