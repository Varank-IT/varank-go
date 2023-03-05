<template>
    <div class="slider-container">
        <div class="slider">

            <!-- slide 1 -->
            <div class="slide">
                <img src="https://media.discordapp.net/attachments/1035213952986140682/1035214164446171259/WhatsApp_Image_2022-10-27_at_5.59.34_PM.jpeg"
                    alt="" />
            </div>

            <!-- slide 2 -->
            <div class="slide">
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214165029175386/WhatsApp_Image_2022-10-27_at_6.11.28_PM.jpeg"
                    alt="" />
            </div>

            <!-- slide 3 -->
            <div class="slide">
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214164085457057/WhatsApp_Image_2022-10-27_at_6.00.07_PM.jpeg"
                    alt="" />
            </div>

            <!-- slide 4 -->
            <div class="slide">
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214163749900408/WhatsApp_Image_2022-10-27_at_6.00.19_PM.jpeg"
                    alt="" />
            </div>

            <!-- slide 5 -->
            <div class="slide">
                <img src="https://cdn.discordapp.com/attachments/1035213952986140682/1035214164756533379/WhatsApp_Image_2022-10-26_at_8.46.49_PM.jpeg"
                    alt="" />
            </div>

            <!-- slide 6 -->
            <div class="slide">
                <img src="https://media.discordapp.net/attachments/1035213952986140682/1035214163372425266/WhatsApp_Image_2022-10-27_at_6.03.14_PM.jpeg"
                    alt="" />
            </div>

            <!-- Control buttons -->
            <button class="btn btn-next">&gt;</button>
            <button class="btn btn-prev">&lt;</button>
        </div>
    </div>
</template>

<style scoped>
/* point and laugh */
/* display: grid; */

.slider-container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.slider {
    width: 100%;
    max-width: 800px;
    height: 650px;
    position: relative;
    overflow: scroll;
    /* overflow: hidden; */
}

.slide {
    width: 100%;
    max-width: 1000px;
    height: 650px;
    position: absolute;
    transition: all 0.5s;
}

.slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.btn {
    position: absolute;
    width: 40px;
    height: 40px;
    padding: 10px;
    border: none;
    border-radius: 50%;
    z-index: 10px;
    cursor: pointer;
    background-color: #fff;
    transition: all 350ms;
    font-size: 18px;
}

.btn:hover {
    background-color: rgb(208, 208, 208);
    width: 50px;
    height: 50px;
}

.btn:active {
    transform: scale(1.1);
}

.btn-prev {
    top: 45%;
    left: 2%;
}

.btn-next {
    top: 45%;
    right: 2%;
}
</style>

<script setup>/* we need a bit of js :sob: */
import { onMounted } from 'vue'
onMounted(() => {
    // Select all slides
    const slides = document.querySelectorAll(".slide");
    console.log(slides)

    // loop through slides and set each slides translateX
    slides.forEach((slide, indx) => {
        slide.style.transform = `translateX(${indx * 100}%)`;
    });

    // select next slide button
    const nextSlide = document.querySelector(".btn-next");

    // current slide counter
    let curSlide = 0;
    // maximum number of slides
    const humanReadableMaxSlides = 5
    let maxSlide = humanReadableMaxSlides - 1;

    // add event listener and navigation functionality
    nextSlide.addEventListener("click", function () {
        // check if current slide is the last and reset current slide
        if (curSlide === maxSlide) {
            curSlide = 0;
        } else {
            curSlide++;
        }

        //   move slide by -100%
        slides.forEach((slide, indx) => {
            slide.style.transform = `translateX(${100 * (indx - curSlide)}%)`;
        });
    });

    // select next slide button
    const prevSlide = document.querySelector(".btn-prev");

    // add event listener and navigation functionality
    prevSlide.addEventListener("click", function () {
        console.log(curSlide)
        // check if current slide is the first and reset current slide to last
        if (curSlide === 0) {
            curSlide = maxSlide;
        } else {
            curSlide--;
        }

        //   move slide by 100%
        slides.forEach((slide, indx) => {
            slide.style.transform = `translateX(${100 * (indx - curSlide)}%)`;
        });
    });
})
</script>
