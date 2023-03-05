<template>
    <header id="header" class="animated slideInDown" :class="{ 'isScrolled': hasScrolled }"
        style="animation-delay:0.8s;">
        <table>
            <tr>
                <td id="logo">V | GO</td>
                <td id="navigation">
                    <a href="">Başvur</a>
                </td>
            </tr>
        </table>
    </header>
</template>

<script>
export default {
    name: 'TheHeader',
    data: () => ({
        hasScrolled: false
    }),
    methods: {
        handleScroll() {
            if (window.innerWidth >= 1) {
                this.hasScrolled = document.body.scrollTop > 80 || document.documentElement.scrollTop > 80;
            }
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.handleScroll);
    }
}
</script>

<style lang="scss" scoped>
/* so this is how vue works -a*/
// yes, every vue component has 3 parts, a template for your haitch tee em el,z a script for your functional shit and a style for your styling shit -m
// also notice how scss can use // for comments -m
// that's awesome! -a
// pro tip: use ctrl+/ to automatically comment/uncomment something -m
// oh, thanks! -a

header {
    width: 100vw;
    padding-top: 1.5vh;
    padding-bottom: 1.5vh;
    position: fixed;
    font-weight: bold;
    background-color: #008cf2;
    box-shadow: none;
    transition: 0.4s ease-in-out;
    z-index: 2;
    color: #ffffff;
}

header.isScrolled {
    background-color: #ffffff;
    color: #008cf2;
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.09);
}


header table {
    width: 100%;
}

#logo {
    width: 20%;
    padding-left: 2vw;
    font-size: 24px;
}

/* i want to die */

#navigation {
    width: 50%;
    padding-right: 2vw;
}

#navigation {
    text-align: right;
}

#navigation a {
    color: inherit;
    text-decoration: none;
    padding: 5px 10px;
    border-bottom: 2px solid transparent;
    margin-left: 4vw;
    transition: 0.4s ease-in-out;
}

#navigation a:hover {
    border-bottom: 2px solid #fff;
}


@media screen and (max-width: 1000px) {

    header {
        /* width: 92vw; */
        width: 100vw;
        /* padding: 6vh 4vw; */
        padding-top: 1.5vh;
        padding-bottom: 1.5vh;
        position: fixed;
        font-weight: bold;
        background: #008cf2;
        box-shadow: none;
        transition: 0.4s ease-in-out;
        z-index: 2;
        color: #ffffff;
    }

    header.isScrolled {
        background-color: #ffffff;
        color: #008cf2;
        box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.15);
    }

    header table {
        width: 100%;
    }

    #logo {
        width: 70%;
        padding-left: 6vw;
        font-size: 18px;
    }

    /* i want to die */

    #navigation {
        width: 70%;
        padding-right: 6vw;
        font-size: 18px;
    }

    #navigation {
        text-align: right;
    }

    #navigation a {
        color: inherit;
        text-decoration: none;
        padding: 5px 10px;
        border-bottom: 2px solid transparent;
        margin-left: 4vw;
        transition: 0.4s ease-in-out;
    }

    #navigation a:hover {
        border-bottom: 2px solid #fff;
    }

}
</style>