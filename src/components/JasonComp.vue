<template>
    <div class="jason">

        <!-- creiamo un'immagine  -->

        <div class="interview">

            <img src="../assets/img/h1-img-01.jpg" alt="">

            <button>
                <img class="arrowleft" src="../assets/img/svg-6.svg">
                <img class="arrowright" src="../assets/img/svg-6.svg">
            </button>

            

        </div>
        <!-- creiamo un div che si andrà a sovrapporre all'immagine di sopra -->

        <div class="jasonFounder">

            <h2>Jason Bickford</h2>
            <p>Found and Executive Director</p>
            <div class="border"></div>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum culpa ullam iure</p>

            <div class="logos">
                
                <i class="fab fa-linkedin"></i>

                <i class="fab fa-facebook"></i>

                <i class="fab fa-twitter-square"></i>
            </div>

            <span class="jasonSign">Jason Brick</span>

        </div>

        <!-- mettiamo un'immagine simil sfondo -->

        <img class="origin" src="../assets/img/svg-4.svg">

       <button class="buttonJason buttonJason1"><i class="fas fa-long-arrow-alt-up"></i></button>

       <button class="buttonJason buttonJason2"><i class="fas fa-long-arrow-alt-up"></i></button>
        
    </div>
</template>

<script>
export default {
  name: 'JasonComp',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

/* stilizziamo le sezioni */
    .jason {
        width: 60%;
        margin: 100px auto 0;
        display: flex;
        position: relative;

        .buttonJason {
                background-color: white;
                border: none;
                border-radius: 50%;
                padding: 10px 15px;
            }

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }

            .buttonJason1 {
                position:absolute;
                right: -290px;
            }

            .buttonJason2 {
                position: absolute;
                right: -290px;
                bottom: 430px;
            }
        
        img {
            width: 100%;
        }

        button {
            background-color: #ff4612;
            display: flex;
            padding: 10px;
            border: none;
            position: absolute;
            bottom: 4px;
            

            img {
                vertical-align: middle;
            }
            
            .arrowleft {
                transform: rotate(180deg);
            }

            .arrowright {
                margin-top: 2px;
            }

        }
        .jasonFounder {
            height: 250px;
            width: 90%;
            background-color: white;
            margin-left: -100px;
            margin-top: 50px;
            padding: 30px;
            z-index: 99;
        }

        .border {
            border-bottom: 2px solid #ff4612;
            width: 10%;
            margin: 20px 0;
        }

        .logos {
            margin-top: 10px;
        }

        .fab:hover {
            color: black;
            cursor: pointer;
        }

        .logos i {
            color: #ff4612;
            font-size: 25px;
            margin-right: 15px;
        }

        .jasonSign {
            float: right;
            color: #ff4612;
            margin-top: -30px;
        }

        .origin {
           filter: invert(1);
           right: -170px;
           bottom: 30px;
           width: 45%;
           position: absolute;
        }
    }
</style>
