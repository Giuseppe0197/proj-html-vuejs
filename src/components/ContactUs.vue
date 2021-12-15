<template>
<div class="contact">

    <div class="sectionInfo">
        
        <!-- creiamo una sezione per mostrare le varie parti del mondo in cui il servizio è attivo -->

        <div class="map">
            <div class="city">
                <h4>New York Coaching</h4>
                <h5>read more</h5>
            </div>

            <img id="USA" src="../assets/img/h1-contact-rev-02.png" alt="">

            <img id="europe" src="../assets/img/h1-contact-rev-02.png" alt="">
            
            <img id="australia" src="../assets/img/h1-contact-rev-02.png" alt="">
        </div>

        <!-- creiamo un form per permettere all'utente di inserire i dati in modo da essere successivavente contattato per evere delle informazioni riguardanti il servizio -->

        <div class="form">
            <h2>Contact Us<span class="dot">.</span></h2>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>

            <div class="border"></div>

            
            <div class="formData">

                <input type="text" placeholder="Your Name">

                <input type="text" placeholder="Your Email">

                <textarea name="" id="" cols="" rows="5" placeholder="Write a message"></textarea>

            </div>

            <button class="send">send<span class="bordersend"></span><img src="../assets/img/svg-6.svg"></button>

        </div>

    </div>

    <!-- sezione con i loghi della pagina -->

    <div class="logos">

        <div v-for="img, i in imgLogo" :key="i" class="logoFirst">

            <img class="logo" :src="require(`../assets/img/${img.firstImg}`)" alt="">
            <img class="logoHover" :src="require(`../assets/img/${img.secondImg}`)" alt="">

        </div>

        <button class="buttonLogo"><i class="fas fa-long-arrow-alt-up"></i></button>

    </div>

</div>
</template>

<script>
export default {
  name: 'ContactUs',
    data () {
        return {
            imgLogo: [
                {
                    'firstImg': 'h4-clients-img-03.png',
                    'secondImg': 'h4-clients-img-04-1.png'
                },

                {
                    'firstImg': 'h4-clients-img-05.png',
                    'secondImg': 'h4-clients-img-06-1.png'
                },

                {
                    'firstImg': 'h4-clients-img-07.png',
                    'secondImg': 'h4-clients-img-08-1.png'
                },

                {
                    'firstImg': 'h4-clients-img-09.png',
                    'secondImg': 'h4-clients-img-10-1.png'
                },

                {
                    'firstImg': 'h4-clients-img-01.png',
                    'secondImg': 'h4-clients-img-02.png'
                }
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .sectionInfo {
        width: 70%;
        margin: 100px auto;
        min-height: 400px;
        display: flex;
        justify-content: space-evenly;

        .map {
            width: 50%;
            background-image: url("../assets/img/h1-contact-rev-01.png");
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
            position: relative;
            margin-right: 50px;
            
            .city {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-70%, - 30%);
                background-color: white;
                padding: 20px;
            }

            #USA {
                position: absolute;
                top: 150px;
                left: 120px;
            }

            #europe {
                position: absolute;
                top: 120px;
                left: 270px;
            }

            #australia {
                position: absolute;
                bottom: 110px;
                right: 70px;
            }
        }

        .form {
            width: 50%;

            h2 {
                font-size: 40px;
            }

            .dot {
                color: #ff4612;
            }

            p {
                color: #B2B2B2;
                font-size: 15px;
                margin: 10px 0 20px;
            }

            .border {
                border-bottom: 2px solid #ff4612;
                width: 50px;
            }
        }

        .formData {
            margin-top: 40px;

            input {
                border: none;
                border-bottom: 1px solid #B2B2B2;
                background-color: #fafafa;
                width: calc(100% / 2 - 10px);
                margin-right: 10px;
                color: #B2B2B2;
            }

            textarea {
                width: 100%;
                margin-top: 20px;
                border: none;
                color: #B2B2B2;
                border-bottom: 1px solid #B2B2B2;
                background-color: #fafafa;
            }
        }

        .send {
            background-color: #ff4612;
            margin-top: 20px;
            color: white;
            border: none;
            padding: 10px 20px;
            text-transform: uppercase;
            font-size: 12px;

            img {
                vertical-align: middle;
                margin-left: 10px;
            }

        .bordersend {
            border-left: 2px solid white;
            margin-left: 15px;
        }

        }
    }

    .logos {
        width: 70%;
        margin: 0 auto;
        padding-bottom: 80px;
        display: flex;
        justify-content: space-between;
        position: relative;

        .buttonLogo {
            position: absolute;
            right: -200px;
            background-color: white;
            border: none;
            border-radius: 50%;
            padding: 10px 15px;

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }
        }

        .logoHover {
            display: none;
        }

        .logoFirst:hover .logo {
            display: none;
        }

        .logoFirst:hover .logoHover {
            display: block;
        }
    }
</style>
