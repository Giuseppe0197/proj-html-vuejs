<template>
    <div class="jason">

        <div class="interview">

            <img src="../assets/img/h1-img-01.jpg" alt="">

            <button>
                <img class="arrowleft" src="../assets/img/svg-6.svg">
                <img class="arrowright" src="../assets/img/svg-6.svg">
            </button>

            

        </div>

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

        <img class="origin" src="../assets/img/svg-4.svg">

       
        
    </div>
</template>

<script>
export default {
  name: 'JasonComp',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .jason {
        width: 60%;
        margin: 100px auto 0;
        display: flex;
        position: relative;
        
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

        .logos i {
            color: #ff4612;
            font-size: 25px;
            margin-right: 15px;
        }

        .jasonSign {
            float: right;
        }

        .origin {
           filter: invert(1);
           right: -170px;
           bottom: 30px;
           width: 45%;
           /* height: 300px; */
           position: absolute;
        }
    }
</style>
