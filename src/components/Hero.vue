<template>
    <section class="landing-section">
        <table id="top_part">
            <tr>
                <td id="landing" class="animated fadeIn" style="animation-delay:1s;">
                    <p id="timer"></p>
                    <h1>Varank Girişimcilik Organizasyonu</h1>
                    <h3>28-30 Nisan</h3>
                    <a class="btn_one" href="">Başvur</a>
                    <!--<a class="social"><i class="fab fa-instagram"></i></a> it aint rendering properly... yet :> -->
                </td>
            </tr>
        </table>
    </section>
</template>

<script>
export default {
    name: 'Hero'
}

// Set the date we're counting down to
var countDownDate = new Date("Apr 28, 2023 08:00:00").getTime();
var x = setInterval(function () {
    var now = new Date().getTime();
    var distance = countDownDate - now;
    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);
    document.getElementById("timer").innerHTML = days + " Gün " + hours + " Saat "
        + minutes + " Dakika " + seconds + " Saniye";
    if (distance < 0) {
        clearInterval(x);
        document.getElementById("timer").innerHTML = "EXPIRED";
    }
}, 1000);

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@500&display=swap');

#top_part {
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    background: #008cf2;
    color: #ffffff;
}

/*#top_part tr td .button {
    width: 50%;
}*/

#landing {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
    padding: 0px 10%;
}

#landing h1 {
    font-size: 45px;
    text-align: center;
    font-family: 'Cinzel', serif;
    color: #ffffff;
}

#landing h2 {
    font-size: 30px;
    text-align: center;
    font-family: 'Cinzel', serif;
    color: #ffffff;
}

#landing h3 {
    font-size: 25px;
    text-align: center;
    font-family: 'Cinzel', serif;
    color: #ffffff;
}

#landing p {
    font-size: 20px;
    text-align: center;
    font-family: 'Cinzel', serif;
    color: #ffffff;
}

#landing table {
    /*   width: 70%; */
    margin-top: 4vh;
}

#landing table tr td {
    /*   width: 20% !important; */
    text-align: left;
}

/*
.social {
    display: inline-block;
    font-size: 18px;
    font-family: 'Poppins', sans-serif;
    color: #ffffff;
    background: linear-gradient(0deg, rgba(93, 200, 232, 1) 0%, rgba(0, 140, 242, 1) 100%);
    padding: 8px 40px;
    border-radius: 80px;
    font-weight: bold;
    margin-left: auto;
    margin-right: auto;
    transition: 0.4s ease-in-out;
    text-decoration: none;
    font-family: 'Cinzel', serif;
}

.social:hover {
    box-shadow: 0px 10px 30px #111822;
    cursor: pointer;
    color: #111822;
    background: #d1ab74;
}
*/
.btn_one {
    display: inline-block;
    font-size: 18px;
    font-family: 'Poppins', sans-serif;
    color: #ffffff;
    background: transparent;
    border: 3px solid #ffffff;
    padding: 8px 40px;
    /*    width: %; */
    border-radius: 80px;
    font-weight: bold;
    margin-top: 50px;
    margin-bottom: 50px;
    margin-left: auto;
    margin-right: auto;
    transition: 0.4s ease-in-out;
    text-decoration: none;
    font-family: 'Cinzel', serif;
}

.btn_one:hover {
    box-shadow: 0px 10px 30px #ffffff;
    cursor: pointer;
    color: #00c6fb;
    background: #ffffff;
}

@media (max-width: 1000px) {

    #top_part {
        border: 0px;
    }

    #top_part tr td {
        width: 100%;
        text-align: center;
    }

    #landing {
        width: 92% !important;
        height: 100vh;
        padding-top: auto !important;
        text-align: center;
        padding: 0px 4%;
    }

    #landing h1 {
        font-size: 30px;
        text-align: center;
        font-family: 'Cinzel', serif;
        color: #ffffff;
    }

    #landing h2 {
        font-size: 20px;
        text-align: center;
        font-family: 'Cinzel', serif;
        color: #ffffff;
    }

    #landing h3 {
        font-size: 15px;
        text-align: center;
        font-family: 'Cinzel', serif;
        color: #ffffff;
    }

    #landing p {
        font-size: 15px;
        text-align: center;
        font-family: 'Cinzel', serif;
        color: #ffffff;
    }

    #landing table {
        width: 100%;
        margin-top: 6vh;
    }

    #landing table tr td {
        text-align: center;
    }

    .btn_one {
        padding: 6px 20px;
        width: 60%;
        margin: 3vh auto;
        background: transparent;
        color: #ffffff;
        text-decoration: none;
        font-family: 'Cinzel', serif;
    }

    .btn_one:hover {
        box-shadow: 0px 1px 1px #ffffff;
        color: #008cf2;
        cursor: pointer;
    }
}
</style>