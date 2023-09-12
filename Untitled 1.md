  
It doesn't work :/, 
HTML :
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>ExistensyGFX</title>

    <link rel="icon" href="img/favicon.ico" type="image/icon type">

    <link rel="stylesheet" href="style.css">

    <script src="script.js"></script>  

    <script

  src="https://code.jquery.com/jquery-1.12.4.min.js"></script>

</head>

<body>

        <div class="everything">

        <header class="sticky">

            <nav>

                <img src="img/EXISTENSY.png" alt="ExistensyGFX" class="logo">

                <ul>

                    <li>

                        <a href="#" class="line">Home</a>

                    </li>

                    <li>

                        <a href="#" class="hoverr">Portfolio</a>

                    </li>

                    <li>

                        <a href="#" class="hoverr">Order</a>

                    </li>

                    <li>

                        <a href="#" class="hoverr big">Manage Orders</a>

                    </li>

                    <li>

                        <a href="#" id="course" class="hoverr">Cartoony GFX Course</a>

                    </li>

                </ul>

                <a href="https://discord.gg/BaPADtmkdg"><img src="img/discord logo white.png" alt="discord" class="discord" id="big-btnd"></a>

                <a href="https://twitter.com/ExistensyGFX"><img src="img/x white.png" alt="x" class="x" id="big-btnx"></a>

            </nav>

        </header>

        <section class="home">

            <div class="home-content">

                <h1>Over <span class="bold">1 BILLION</span></h1>

                <h1>Visits Reached!</h1>

                <div class="container"><h3>High CTR Icons and thumbnails</h3></div>

                <div class="btn-box card">

                    <a href="#">

                        ORDER HERE

                    </a>

                </div>

            </div>

        </section>

        <div class="containeer">

            <div class="card">

                <div class="content">

                    <div class="counter-text">

                        <h1 class="counter">88.2</h1><h1 class="M">M+</h1>

                    </div>

                    <h2>Type or Die</h2>

                </div>

            </div>

        </div>

        <div class="exiicons">

            <img src="img/img1.png" alt="Existensy work" class="img1">

            <img src="img/img2.png" alt="Existensy work" class="img2">

            <img src="img/img3.png" alt="Existensy work" class="img3">

            <img src="img/img4.png" alt="Existensy work" class="img4">

            <img src="img/img5.png" alt="Existensy work" class="img5 loop-img">

            <img src="img/img6.png" alt="Existensy work" class="img6">

            <img src="img/img7.png" alt="Existensy work" class="img7">

            <img src="img/img8.png" alt="Existensy work" class="img8">

        </div>

        <img src="img/square.png" alt="square" class="cut-square">

        <div class="radial-line" style="width: 100%; height: 1px;"></div>

        <script type="text/javascript" src="vanilla-tilt.js"></script>

        <script>

            VanillaTilt.init(document.querySelector(".card"), {

        max: 25,

        speed: 400

    });

        </script>

        <script src="http://cdnjs.cloudflare.com/ajax/libs/waypoints/2.0.3/waypoints.min.js"></script>

        <script src="jquery.counterup.min.js"></script>

        <script>

        jQuery(document).ready(function($){

            $('.counter').counterUp({

    delay: 10.2,

    time: 2000

});

        });

        </script>

        </div>

        <section class="cut-part">

            <section class="question-order">

                <h1 class="question-text1">ExistensyGFX</h1>

                <h2 class="question-text2">WHY ORDER FROM ME?</h2>

            </section>

            <section class="CTRincrease-img">

                <img src="img/old.png" alt="old" class="ccu-img-1">

                <img src="img/img8.png" alt="8" class="ccu-img-2">

                <h1 class="old">OLD</h1>

                <div class="neew">

                    <h1>NEW</h1>

                </div>

                <h1 class="old-ccu counter">284</h1>

                <h1 class="new-ccu">5.1K</h1>

                <div class="ccu-icons">

                    <img src="img/CCU.png" id="ccu1">

                    <img src="img/CCU.png" id="ccu2">

                </div>

                <h1 id="ccu-under">not up to date</h1>

            </section>

            <section class="CTR-show">

                <img src="img/CTR background.png" alt="CTR" class="CTR-back">

                <img src="img/CTR _.png" alt="CTR" class="CTR-front">

            </section>

        </section>

</body>

</html>
CSS :
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&family=Tilt+Warp&display=swap');

  

*,

*::before,

*::after {

    padding: 0;

    margin: 0;

    box-sizing: border-box;

}

  

html {

    position: relative;

    width: 100%;

    height: 200vh;

    overflow-x: hidden;

    background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);

}

  

::-webkit-scrollbar {

    width: 10px;

}

  

::-webkit-scrollbar-track {

    background: #10161f;

}

  

::-webkit-scrollbar-thumb {

    background: linear-gradient(

        transparent,

        rgba(255,255,255, 0.3)

    );

    border-radius: 5px;

    backdrop-filter: blur(10px);

    /*box-shadow:

    0 0 10px #58606b,

    0 0 40px #58606b,

    0 0 80px #58606b,

    0 0 120px #58606b;*/

}

  

/*html:before {

    content: '';

    position: absolute;

    bottom: 0;

    left: 0;

    width: 100%;

    height: 2300px;

    background: radial-gradient(ellipse at bottom, #10161f 0%, #090a0f 100%);

    clip-path: polygon(0 55%, 100% 46%, 100% 100%, 0% 100%);

}*/

  
  

body {

    font-family: 'Poppins', sans-serif;

}

  

/*header {

    width: 100%;

    border-bottom: 1px solid rgba(255, 255, 255, 0.1);

}*/

  

.logo {

    width: 150px;

    margin-left: -25px;

  }

  

.x {

    width: 20px;

    margin-left: -150px;

    cursor: pointer;

}

  

.discord {

    width: 27px;

    margin-right: -215px;

    cursor: pointer;

}

header {

    width: 100%;

  }

  
  

header nav {

    max-width: 1400px;

    margin: 0 auto;

    padding: 0 2rem;

    margin-top: 30px;

    display: flex;

    justify-content: space-between;

    align-items: center;

  }

header ul {

    display: flex;

    list-style: none;

    align-items: center;

    margin: 0;

    padding: 0;

  }

  
  

header a:after {

    content: "";

    position: absolute;

    width: 90%;

    height: 1px;

    bottom: -8.5px;

    left: 0;

    background-color: #ffff;

    border-radius: 10px;

    transform: scaleX(0);

    transition: transform 0.5s ease-out;

}

header a:hover:after {

    transform: scaleX(0);

    transform-origin: center;

    align-content: center;

    width: 90%;

    height: 1px;

    bottom: -8.5px;

}

  
  

#course {

    font-weight: 700;

    text-shadow: 0 0 5px rgba(255, 255, 255, 0.8), 0 0 30px #fff;

}

header a {

    text-decoration: none;

    color: white;

    padding: 0 1.5rem;

    font-weight: 300;

    font-size: 0.9rem;

    position: relative;

  }

.big {

    font-size: 0.83rem;

    transition: font-size 0.3s ease-in-out;

  }

.big:hover {

    font-size: 0.95rem;

  }

  

#big-btnd {

    transition: width 0.2s ease-in-out;

  }

#big-btnd:hover {

    width: 35px;

  }

  

  #big-btnx {

    transition: width 0.3s ease-in-out;

  }

#big-btnx:hover {

    width: 29px;

  }

  

/* Add these styles to your existing CSS */

  

.sticky {

    position: sticky;

    top: 0;

    background-color: transparent; /* Initially transparent */

    z-index: 100;

    margin-top: 15px;

    transition: background-color 0.3s ease-in-out;

    padding-bottom: 9.5px;

}

  

.sticky.scrolled {

    background-color: rgba(14, 18, 26, 0.5);

    backdrop-filter: blur(10px);

    border-bottom: 1px solid rgba(255, 255, 255, 0.1);

}

  

.sticky nav {

    max-width: 1400px;

    margin: 0 auto;

    padding: 0 2rem;

}

  

  

.hoverr {

    display: inline-block;

    padding-bottom: 0.25rem;

    position: relative;

    text-decoration: none;

}

  

.hoverr::after {

    content: "";

    position: absolute;

    left: 0;

    bottom: -8.5px;

    width: 90%;

    height: 1px;

    background-color: white;

    transform: scaleX(0);

    transition: transform 0.25s ease-out;

}

  

.hoverr:hover::after {

    transform: scaleX(1);

}

  

.line {

    text-decoration: none;

    position: relative;

    color: white;

}

  

.line::before {

    content: "";

    position: absolute;

    width: 50%;

    height: 2px;

    bottom: -12px;

    border-radius: 5px;

    left: 23px;

    background-color: white; /* Color of the underline */

    transform: scaleX(1);

    transform-origin: bottom left;

    transition: 0.25s ease-out; /* Remove the transition effect */

}

  

.home {

    color: #fff;

    height: 100vh;

    display: flex;

    align-items: center;

    padding: 0 10%;

}

  

.home-content {

    max-width: 600px;

    margin-top: 150px;

    position: relative;

    left: -130px;

}

  

.home-content h1 {

    font-size: 70px;

    font-weight: normal;

}

  

.bold {

    font-size: 75px;

    font-weight: bolder;

}

  

.container {

    display: inline-block;

}

  

.home-content h3 {

    font-size: 18px;

    font-weight: normal;

    color: #949597;

    border-right: 2px solid;

    width: 100%;

    white-space: nowrap;

    overflow: hidden;

    margin: 20px 0 40px;

    animation:

        typing 5s 1,

        cursor .4s step-end infinite alternate;

}

  

@keyframes cursor {

    50% {border-color: transparent;}

}

  

@keyframes typing {

    0% {

        width: 0;

    }

    40% {

        width: 0;

    }

    100% {

        width: 100%;

    }

}

  

.home-content .btn-box {

    display: flex;

    justify-content: space-between;

    width: 400px;

    height: 60px;

}

  

.btn-box a {

    display: inline-flex;

    justify-content: center;

    align-items: center;

    width: 240px;

    height: 100%;

    background: rgba(169, 13, 248, 1);

    border: 2px solid rgb(169, 13, 248, 1);

    border-radius: 10px;

    font-size: 19px;

    color: white;

    text-decoration: none;

    font-weight: 600;

    letter-spacing: 1px;

    overflow: hidden;

    backdrop-filter: blur(5px);

    box-shadow:

    0 0 15px #a90df8,

    0 0 50px rgb(0, 0, 0, 0.3);

    transition: background 0.3s, transform 0.3s, box-shadow 0.3s ease;

}

  
  

.btn-box a:hover {

    background-color: #ba31ff;

    box-shadow:

    0 0 10px #b01ef8,

    0 0 40px #b01ef8,

    0 0 80px #b01ef8,

    0 0 120px #b01ef8;

    transition-delay: 0.2s;

    transform: scale(1.1);

}

  
  
  

.home {

    color: #fff;

    height: 100vh;

    display: flex;

    align-items: center;

    padding: 0 10%;

    position: relative;

    margin-top: -125px;

    left: 150px;

}

  

.exiicons {

    display: flex;

    align-items: center;

    margin-top: 135px;

}

  
  
  

.exiicons img {

    width: 170px;

    height: auto;

    transform: translateY(-60px);

}

  
  

.exiicons .img5 {

    position: absolute;

    margin-top: -1400px;

    right: 585px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s, animation;

}

  

.exiicons .img7 {

    position: absolute;

    margin-top: -1250px;

    right: 800px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s;

}

  

.exiicons .img6 {

    position: absolute;

    margin-top: -1250px;

    right: 380px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s;

}

  

.exiicons .img8 {

    position: absolute;

    margin-top: -1010px;

    right: 590px;

    background-clip: content-box;

    filter: drop-shadow(0 0 5px #F59A02) drop-shadow(0 0 100px #F59A02);

    overflow: hidden;

    animation: changeGlowColor 10s infinite;

}

  

@keyframes changeGlowColor {

    0% {

        filter: drop-shadow(0 0 5px #f72f7c) drop-shadow(0 0 100px #f72f7c);

    }

    25% {

        filter: drop-shadow(0 0 5px #F59A02) drop-shadow(0 0 100px #F59A02);

    }

    50% {

        filter: drop-shadow(0 0 5px #2f9df7) drop-shadow(0 0 100px #2f9df7);

    }

    75% {

        filter: drop-shadow(0 0 5px #f11a1a) drop-shadow(0 0 100px #f11a1a);

    }

    100% {

        filter: drop-shadow(0 0 5px #f72f7c) drop-shadow(0 0 100px #f72f7c);

    }

}

  
  

.exiicons .img4 {

    position: absolute;

    margin-top: -860px;

    right: 380px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s;

}

  

.exiicons .img2 {

    position: absolute;

    margin-top: -860px;

    right: 800px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s;

}

  

.exiicons .img1 {

    position: absolute;

    margin-top: -475px;

    right: 800px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    clip-path: polygon(1% 0, 100% 0, 100% 58%, 0 68.5%);

    transition: filter 0.3s;

}

  

.exiicons .img3 {

    position: absolute;

    margin-top: -625px;

    right: 590px;

    filter: blur(0.9px);

    overflow: hidden;

    background-clip: content-box;

    clip-path: polygon(1% 0, 100% 0, 100% 88.5%, 0 99.5%);

    transition: filter 0.3s;

}

  

.exiicons .img1:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img2:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img3:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img4:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img5:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img6:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.exiicons .img7:hover {

    filter: blur(0px);

    transition-delay: 0.2s;

}

  

.containeer {

    position: relative;

    display: flex;

    justify-content: center;

    max-width: 1200x;

    flex-wrap: wrap;

    z-index: 1;

}

  

.containeer .card .content h1, h2{

    text-align: center;

    margin-top: 10px;

}

  

.containeer .card {

    position: absolute;

    width: 140px;

    height: 60px;

    margin: -390px;

    margin-left: 260px;

    box-shadow: 20px 20px 50px rgba(0, 0, 0, 0.5);

    border-radius: 15px;

    background: rgba(255, 255, 255,0.8);

    overflow: hidden;

    display: flex;

    justify-content: center;

    align-items: center;

    border-top: 1px solid rgba(255, 255, 255, 0.5);

    border-left: 1px solid rgba(255, 255, 255, 0.5);

    backdrop-filter: blur(5px);

}

  

.containeer .card .content {

    padding: 20px;

    text-align: center;

}

  

.containeer .card .content h1 {

    font-size: 23px;

    font-weight: 3000;

    margin-top: 0px;

    color: #0C0F16;

}

  

.containeer .card .content .counter-text {

    display: flex;

    align-items: center;

    justify-content: center;

}

  

.containeer .card .content .counter-text h1 .M {

    font-family: 'Poppins', sans-serif;

    font-size: 23px;

    font-weight: 300;

    margin-top: 0px;

    color: #0C0F16;

}

  
  

.containeer .card .content h2 {

    font-size: 12px;

    font-weight: normal;

    margin-top: -7px;

    color: #0C0F16;

}

  

h1 .bold {

    color: transparent;

    -webkit-text-stroke: 0.8px #fff;

    background: url(img/back.png);

    -webkit-background-clip: text;

    background-position: 0 0;

    animation: back 20s linear infinite;

}

  

@keyframes back {

    100% {

        background-position: 2000px 0;

    }

}

  

/*.cut-square {

    width: 100%;

    height: 6px;

    position: absolute;

    margin-top: -0px;

    right: 0px;

    overflow: hidden;

    background-clip: content-box;

    transition: filter 0.3s;

}*/

  

.radial-line{

    background-image: radial-gradient(circle, #fff 23%, #0B0D13);

    box-sizing: border-box;

    margin-top: -1075px;

    transform: rotate(-6.15deg)

  }

  
  

.loop-image {

    position: absolute;

    width: 100%;

    opacity: 1;

    transition: opacity 1s ease-in-out;

}

  

.loop-image {

    position: absolute;

    width: 100%;

    opacity: 1;

    transition: opacity 5s ease-in-out; /* Adjust the transition duration as needed */

}

  
  

.cut-part {

    width: 100%;

    margin-top: -200px;

    height: 1500px;

    background: radial-gradient(ellipse at bottom, #090a0f 0%,  #10161f 100%);

    clip-path: polygon(0 20.19%, 100% 6.43%, 100% 100%, 0% 100%);

}

  

.question-order {

    display: flex;

    flex-direction: column;

    align-items: center;

    justify-content: center;

    height: 100vh;

}

  

.question-text1 {

    text-align: center;

    margin: 10px;

    color: #3F4143;

    font-weight: 300;

    margin-top: -150px;

}

  

.question-text2 {

    text-align: center;

    font-size: 60px;

    color: white;

    font-weight: 540;

    margin-top: -10px;

    letter-spacing: -1px;

}

  
  
  

.ccu-img-1 {

    width: 135px;

    height: auto;

    margin-left: 500px;

}

  

.ccu-img-2 {

    width: 135px;

    height: auto;

    margin-left: 70px;

    margin-top: 30px;

}

  

.CTRincrease-img {

    margin-top: -400px;

}

  

.old {

    color: #5B5C5E;

    margin-top: -193px;

    font-size: 23px;

    font-weight: 540;

    margin-left: 543px;

}

  

.neew {

    color: #05D41A;

    position: relative;

    margin-top: -38px;

    font-size: 23px;

    font-weight: 540;

    margin-left: 750px;

    text-shadow: 0 0 5px #05D41A, 0 0 30px #05D41A;

}

  

.old-ccu {

    color: #5B5C5E;

    position: relative;

    margin-top: 159px;

    font-size: 20px;

    font-weight: 540;

    margin-left: 554px;

}

  

.new-ccu {

    color: #fff;

    position: relative;

    margin-top: -28.5px;

    font-size: 20px;

    position: absolute;

    font-weight: 540;

    margin-left: 767px;

}

  

.ccu-icons {

    margin-top: -27.4px;

    height: auto;

  

}

  

#ccu1 {

    position: absolute;

    margin-left: 533px;

    height: auto;

    width: 16px;

    opacity: 0.3;

    filter: saturate(50%);

}

  

#ccu2 {

    position: absolute;

    margin-top: 2.5px;

    height: auto;

    width: 16px;

    margin-left: 746px;

}

  

#ccu-under {

    color: #3f4246;

    position: absolute;

    margin-left: 745px;

    margin-top: 28.5px;

    font-size: 9px;

    font-weight: 500;

}

  

.CTR-back {

    height: auto;

    width: 300px;

    margin-top: 180px;

    margin-left: 535px;

}

  

.CTR-front {

    position: relative;

    height: auto;

    width: 300px;

}