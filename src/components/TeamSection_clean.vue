<template>
    <div class="carousel">
        <div class="carousel-center">
            <div class="carousel-body">
                <img src="https://media.discordapp.net/attachments/1035213952986140682/1035214164446171259/WhatsApp_Image_2022-10-27_at_5.59.34_PM.jpeg"
                    id="carousel-item" />
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214165029175386/WhatsApp_Image_2022-10-27_at_6.11.28_PM.jpeg"
                    id="carousel-item" />
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214164085457057/WhatsApp_Image_2022-10-27_at_6.00.07_PM.jpeg"
                    id="carousel-item" />
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214163749900408/WhatsApp_Image_2022-10-27_at_6.00.19_PM.jpeg"
                    id="carousel-item" />
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214164756533379/WhatsApp_Image_2022-10-26_at_8.46.49_PM.jpeg"
                    id="carousel-item" />
                <img src="https://media.discordapp.net/attachments/1035213952986140682/1035214163372425266/WhatsApp_Image_2022-10-27_at_6.03.14_PM.jpeg"
                    id="carousel-item" />
            </div>
        </div>
        <div class="carousel-btns">
            <button id="carousel-next">next</button>
            <button id="carousel-prev">prev</button>
        </div>
    </div>
</template>

<style scoped>
.carousel-body>img:first-of-type {
    display: block;
}

.carousel-body>img {
    display: none;
    max-width: 50%;
}

.carousel-center {
    transform: translateX(25%);
}

.carousel-body {
    display: flex;
    flex-direction: row;
    justify-content: center;
    overflow-x: scroll;
}

#carousel-item {
    transition: transform 2s;
    transform: translateX(0%);
}
</style>

<script setup>/* we need a bit of js :sob: */
import { onMounted } from 'vue'
onMounted(() => {
    const selector = document.querySelectorAll("#carousel-item")

    let currItem = 0;

    for (let i = 0; i < selector.length; i++) {
        // selector[i]
    }
    selector[0].style.display = "block";
    selector[1].style.display = "block";

    document.getElementById("carousel-prev").addEventListener("click", async () => {
        if (currItem < 1) return;
        console.log(`start move: ${currItem}`)
        selector[currItem].style.transform = "translateX(0%)";
        currItem--;
        selector[currItem].style.transform = "translateX(0%)";
        console.log(`end move: ${currItem}`)
    })
    document.getElementById("carousel-next").addEventListener("click", async () => {
        if (currItem === selector.length) return;
        console.log(`start move: ${currItem}`)
        try {
            selector[currItem - 1].style.display = "none";
        } catch (e) { }
        selector[currItem].style.display = "block";
        selector[currItem].style.transform = "";
        selector[currItem + 1].style.display = "block";
        selector[currItem].style.transform = "translateX(-100%)";
        currItem++;
        selector[currItem].style.transform = "translateX(-100%)";
        console.log(`end move: ${currItem}`)
    })
})
</script>
