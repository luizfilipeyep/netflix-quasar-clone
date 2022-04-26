<template>
<div class="container">
    <header>
        <a class="logo" href="#">
            <img src="./assets/netlfix-logo.svg" alt="logo-netflix">
        </a>
        <a href="#">Séries</a>
        <a href="#">Filmes</a>
        <a href="#">Minha lista</a>
    </header>
    <section class="hero"></section>
    <nav class="float"></nav>
</div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'App'
})
</script>

<style lang="scss">
body {
    background: $dark;
    font-family: Arial, Helvetica, sans-serif;
}

.container {
    width: 100vw;
    height: 100vh;
    position: relative;
}

header {
    width: 100%;
    height: 50px;
    background: transparent;
    position: fixed;
    z-index: 1000;

    display: flex;
    justify-content: space-around;
    align-items: center;

    a.logo {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    a {
        color: $white;
        font-size: 14px;
        text-decoration: none;
        padding: 8px 16px;
    }
}

section.hero {
    width: 100%;
    height: 401px;
    background: blue;
}

nav.float {
    width: 100%;
    height: 50px;
    background: red;
}
</style>