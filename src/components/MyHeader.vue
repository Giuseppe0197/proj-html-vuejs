<template>
  <header>
      <div>
          <!-- creiamo un ciclo for per stampare dinamicamente le voci di menu -->
          <MyHeaderSub
          v-for="list, i in headerList"
          :key="i"
          :details="list" />
      </div>

      <!-- creiamo una parte simil jumbo che conterrà tutte le informazioni relative all'header -->

      <div class="team">

        <img class="arrowteam arrowteamleft" src="../assets/img/svg-6.svg">

        <div class="ourteam">

            <h2>Our Team <span class="dot">.</span></h2>

            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque, corporis? Assumenda porro, amet voluptatibus, consequuntur dolorum.</p>

            <button class="read">read more <span class="borderread"></span><img src="../assets/img/svg-6.svg"></button>
            <button class="purchase">purchase <span class="borderpur"></span><img src="../assets/img/svg-6.svg"></button>
        </div>

        <img class="arrowteam arrowteamrigth" src="../assets/img/svg-6.svg">
    </div>

  </header>
</template>

<script>
/* importiamo il sotto componente con il quale popoleremo le voci di menu */
import MyHeaderSub from '@/components/MyHeaderSub.vue'

export default {
  name: 'MyHeader',
  components: {
      MyHeaderSub
  },
  data() {

      return {
          /* creiamo un'array che andrà riportata nel sotto componente tramite props */
          headerList: [
              {
                  'image': 'logo-img-01.png',
                  'imageArrow': 'svg-6.svg',
                  'home': 'homes',
                  'page': 'pages',
                  'blog': 'blog',
                  'shop': 'shop',
                  'event': 'events',
                  'element': 'elements',

              }
          ]
      }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

/* mettiamo un'immagine di sfondo all'header */

    header {
        background-image: url("../assets/img/rev-slider-main-home-img-03.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        height: 750px;

        /* usaimo un filter invert per mettere le frecce desiderate di colore nero */

        img {
            filter: invert(1);
            
        }

        .arrowteam {
            filter: invert(1);
            margin-top: 30px;
        }

        /* andiamo a stlizzare la parte dell'header che contiene le informazioni con i bottoni */

        .team {
            width: 90%;
            margin: 170px auto 0;
        }

        .arrowteamleft {
            transform: rotate(180deg);
            float: left;
        }

        .ourteam {
            float: left;
            margin-left: 150px;
            width: 35%;

            .dot {
                color: #ff4612;
            }

            h2 {
                font-size: 50px;
            }

            p {
                color: #ccc;
                margin: 20px 0;
            }
            
            button {
                border: none;
                padding: 10px;
                text-transform: uppercase;
                font-size: 12px;

                img {
                    vertical-align: middle;
                    margin-left: 10px;
                }

                .borderread {
                    border-left: 2px solid black;
                    margin-left: 15px;
                    
                }

                .borderpur {
                    border-left: 2px solid white;
                    margin-left: 15px;
                }
            }

            .read {
                background-color: white;
            }

            .purchase {
                background-color: #ff4612;
                margin-left: 30px;
                color: white;

                img {
                    filter: invert(0);
                }
            }
        }

        .arrowteamrigth {
            float: right;
        }

    }

</style>
