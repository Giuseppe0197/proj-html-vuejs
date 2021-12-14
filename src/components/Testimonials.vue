<template>
<div class="testimonials">

    <!-- creiamo la sezione che contiene il titolo e l'immagine con le informazioni del testimonial -->

    <div class="testimonialinfo">
        <h2>Testimonials.</h2>
        <button class="buttonTestimonial"><i class="fas fa-long-arrow-alt-up"></i></button>

        <div class="testimonialimage">
            <img class="arrowleft" src="../assets/img/svg-6.svg" alt="">
            <div class="testImg">
                <img src="../assets/img/h3-img-04.png" alt="">

                <h4>Cynthia Clark</h4>

                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem quidem, deleniti inventore nihil ad temporibus beatae dolorum harum esse soluta</p>

                <div class="pages">
                    <span>01</span>
                    <div class="page1"></div>
                    <div class="pagesremained"></div>
                    <span>03</span>
                </div>
            </div>
            <img class="arrowright" src="../assets/img/svg-6.svg" alt="">
        </div>
    </div>

    <!-- creiamo una sezione che funziona da video player per un'introduzione alla pagina e al servizio -->

    <div class="videoplay">

       
            <i class="fas fa-play"></i>

            <button class="buttonplay buttonplay1"><i class="fas fa-long-arrow-alt-up"></i></button>

            <button class="buttonplay buttonplay2"><i class="fas fa-long-arrow-alt-up"></i></button>

            <div class="containerorigin">

                <img class="origins" src="../assets/img/svg-8.svg" alt="">

            </div>

            <div class="containershopping">

                <img class="shopping" src="../assets/img/svg-7.svg" alt="">

            </div>

        

    </div>

</div>
</template>

<script>
export default {
  name: 'Testimonials',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .testimonialinfo {
        background-color: #1E1C1C;
        text-align: center;
        position: relative;
        
        h2 {
            color: #181515;
            font-size: 150px;
        }

        .buttonTestimonial {
            background-color: white;
            border: none;
            border-radius: 50%;
            padding: 10px 15px;
            position:absolute;
            right: 20px;
            top: 60px;

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }
        }

        .arrowleft {
            transform: rotate(180deg);
            width: 40px;
            height: 40px;
        }

        .arrowright {
            width: 40px;
            height: 40px;
        }
    }

    .testimonialimage {
        width: 90%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;

        .testImg {
            margin-top: -50px;
            text-align: center;
            width: 40%;

            h4 {
                margin: 20px 0;
                color: white;
            }

            p {
                margin-bottom: 20px;
                color: #B2B2B2;
            }
        }

        .pages {
            display: flex;
            justify-content: center;
            margin-bottom: 50px;

            span {
                color: #B2B2B2;
            }
        }

        .page1{
            border-bottom: 2px solid #737272;
            width: 30px;
            align-self: center;
            margin-left: 10px;
        }

        .pagesremained {
            border-bottom: 2px solid #2F2D2D;
            width: 60px;
            align-self: center;
            margin-right: 10px;
        }
    }

    .videoplay {
        background-image: url("../assets/img/h1-img-04.jpg");
        height: 750px;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;

        .fa-play {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            font-size: 40px;
            color: white;
        }

        .buttonplay {
            background-color: white;
            border: none;
            border-radius: 50%;
            padding: 10px 15px;

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }
        }

        .buttonplay1 {
            position: absolute;
            right: 5px;
            top: 150px;
        }

        .buttonplay2 {
            position: absolute;
            right: 5px;
            bottom: -15px;
        }


        .containerorigin {
            background-color: #EF2853;
            width: 30px;
            text-align: center;
            padding: 2px;
            position: absolute;
            top: -10px;
            right: 0;

            .origins {
                width: 20px;
                filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(209deg) brightness(117%) contrast(190%);
            }
        }

        .containershopping {
            background-color: white;
            width: 30px;
            text-align: center;
            padding: 2px;
            position: absolute;
            top: 25px;
            right: 0;

            .shopping {
                width: 20px;
            }

        }


    }
</style>
