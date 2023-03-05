<template>
    <TheHeader />
    <MainView />
    <TheFootie />

    <a href="#"><button id="topBtn" title="Go to top"><img class="svg" src="./assets/arrow-up-solid.svg" /></button></a>
</template>

<script setup>
import TheHeader from './components/TheHeader.vue';
import MainView from './views/MainView.vue';
import TheFootie from './components/TheFootie.vue';

import { onMounted } from 'vue'

onMounted(() => {
    // Get the button:
    let mybutton = document.getElementById("topBtn");

    // When the user scrolls down 20px from the top of the document, show the button
    // todo: comment out on production! window.onscroll = function () { scrollFunction() };

    function scrollFunction() {
        if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
            mybutton.style.display = "block";
        } else {
            mybutton.style.display = "none";
        }
    }
})
</script>

<style>
/* yayyy */

@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');



body {
    font-family: 'Open Sans', sans-serif;
    padding: 0px;
    margin: 0px;
    max-width: 100vw;
    overflow-x: hidden;
    scroll-behavior: smooth;
}

#topBtn {
    display: none;
    position: fixed;
    bottom: 20px;
    right: 30px;
    z-index: 99;
    border: none;
    outline: none;
    background-color: red;
    color: white;
    cursor: pointer;
    padding: 15px;
    /*border-radius: 10px;*/
    border-radius: 5rem;
    font-size: 18px;
    transition: background-color 350ms;
}

#topBtn:hover {
    background-color: #555;
}

.svg {
    width: 25px;
    height: 25px;
    -webkit-filter: invert(100%);
    /* safari 6.0 - 9.0 */
    filter: invert(100%);
    padding: 0;
    margin: 0;
}

.wife,
.women-in-general {
    /* excluding aegean chicks */
    right: 100%;
    margin: 0;
}

::placeholder {
    color: #000;
}

button:focus {
    outline: none;
}

::-webkit-scrollbar {
    width: 5px;
    height: 5px;
}

::-webkit-scrollbar-track {
    background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
    background: rgb(0, 0, 0);
}

::-webkit-scrollbar-thumb:hover {
    background: rgba(0, 0, 0, 0.8);
}

/*@media (prefers-color-scheme: dark) {

    night owl UwU
    body {
        background-color: black;
        color: white;
    }

    tr:nth-child(even) {
        background-color: grey !important;
    }
}*/
</style>
