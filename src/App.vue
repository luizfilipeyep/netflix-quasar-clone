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

    <section class="hero">
        <img src="./assets/stranger-things-poster.png" alt="stranger-things-poster">

        <div class="hero-info">
            <img src="./assets/stranger-things-logo.svg" alt="stranger-things-logo">

            <div class="hero-tags">
                <ul>
                    <li>Sinistro</li>
                    <li>Empolgante</li>
                    <li>Adolescente</li>
                </ul>
            </div>

            <div class="hero-options">
                <a class="my-list-button">
                    <img src="./assets/icons/plus-faw-icon.svg" alt="plus-faw-icon">
                    Minha lista
                </a>
                <a class="play-button">
                    <img src="./assets/icons/play-faw-icon.svg" alt="play-faw-icon">
                    Assistir
                </a>
                <a class="details-button">
                    <img src="./assets/icons/info-fi-icon.svg" alt="info-fi-icon">
                    Detalhes
                </a>
            </div>
        </div>
    </section>

    <nav class="float">
        <a class="active" href="#">
            <img src="./assets/icons/home-fi-icon.svg" alt="home-fi-icon">
            Início
        </a>
        <a href="#">
            <img src="./assets/icons/search-fi-icon.svg" alt="search-fi-icon">
            Buscar
        </a>
        <a href="#">
            <img src="./assets/icons/tv-faw-icon.svg" alt="tv-faw-icon">
            Em breve
        </a>
        <a href="#">
            <img src="./assets/icons/download-faw-icon.svg" alt="download-faw-icon">
            Download
        </a>
        <a href="#">
            <img src="./assets/icons/bars-faw-icon.svg" alt="bars-faw-icon">
            Mais
        </a>
    </nav>
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
    height: auto;
    position: relative;

    img {
        width: 100%;
        height: auto;
    }

    .hero-info {
        width: 100%;
        height: 176px;
        position: absolute;
        z-index: 2;
        bottom: 0;
        background: $gradient;

        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;

        img {
            width: 188px;
            height: auto;
            position: relative;
        }

        .hero-tags {
            color: white;
            font-size: 12px;

            ul {
                list-style: none;

                display: flex;
                align-items: center;
                justify-content: center;
                gap: 18px;
                margin-left: -40px;

                li::before {
                    content: "\2022";  /* Add content: \2022 is the CSS Code/unicode for a bullet */
                    color: $red; /* Change the color */
                    font-weight: bold; /* If you want it to be bold */
                    display: inline-block; /* Needed to add space between the bullet and the text */
                    width: 1em; /* Also needed for space (tweak if needed) */
                    margin-left: -1em; /* Also needed for space (tweak if needed) */
                }
                li:nth-child(1)::before {
                    content: ""
                }
            }
        }

        .hero-options {
            width: 100%;
            height: 43px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 25px;

            .my-list-button {
                img {
                    width: 15px;
                }

                width: 35px;
                height: 35px;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                color: white;
                font-size: 10px;
                font-weight: bold;
                white-space: nowrap;
                border-radius: 50px;
            }

            .play-button {
                img {
                    width: 11px;
                }

                font-size: 10px;
                font-weight: bold;
                outline: none;
                color: $black;
                text-decoration: none;
                background: $white;
                border-radius: 2px;
                width: 100px;
                height: 25px;
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 10px;
            }

            .details-button {
                img {
                    width: 15px;
                }

                width: 35px;
                height: 35px;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                color: white;
                font-size: 10px;
                font-weight: bold;
                white-space: nowrap;
                border-radius: 50px;
            }
        }
    }
}

nav.float {
    width: 100%;
    height: 50px;
    background: $darker;
    position: fixed;
    z-index: 1000;
    bottom: 0;

    display: flex;
    justify-content: space-evenly;
    align-items: center;

    a {
        width: 50px;
        height: 50px;
        
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        color: white;
        text-decoration: none;
        font-size: 10px;

        opacity: .5;
    }
    a.active {
        opacity: 1;
    }
}
</style>