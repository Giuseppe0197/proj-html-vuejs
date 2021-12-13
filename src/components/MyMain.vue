<template>
    <main>
      <div class="specialties">

        <h2>Our spacialties <span class="dot">.</span></h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>

        <div class="border"></div>

        <div class="spec">

            <div v-for="spec, i in imagesSpecialties" :key="i" class="specDiv">

                <div class="imageSpec"><img :src="require(`../assets/img/${spec.image}`)"></div>

                <h3>{{spec.titleImg}}</h3>

                <p>{{spec.paragraph}}</p>

            </div>

        </div>


      </div>

      <JasonComp/>

    </main>

</template>

<script>
import JasonComp from '@/components/JasonComp.vue'

export default {
  name: 'MyMain',
  components: {
      JasonComp
  },
  data() {
      return {
          imagesSpecialties: [
              {
                  'image': 'svg-0.svg',
                  'titleImg': 'Knowing',
                  'paragraph':'lorem ipsum dolor sit amet, quis consect'
              },

              {
                  'image': 'svg-1.svg',
                  'titleImg': 'Selling',
                  'paragraph':'lorem ipsum dolor sit amet, quis consect'
              },

              {
                  'image': 'svg-2.svg',
                  'titleImg': 'Learning',
                  'paragraph':'lorem ipsum dolor sit amet, quis consect'
              },

              {
                  'image': 'svg-3.svg',
                  'titleImg': 'Contact',
                  'paragraph':'lorem ipsum dolor sit amet, quis consect'
              }
          ]
      }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

main {
    /* background-color: #fafafa; */

    .specialties {
        background-color: white;
        width: 90%;
        margin: -40px auto 0;
        height: 500px;
        text-align: center;

        h2 {
            font-size: 35px;
            padding-top: 90px;
        }

        p {
            color: #BBBBBB;
            margin-top: 20px;
        }

        .dot {
                color: #ff4612;
            }

        .border {
            border-bottom: 2px solid #ff4612;
            width: 3%;
            margin: 20px auto 0;
        }

        .spec {
            display: flex;
            justify-content: space-evenly;
            width: 90%;
            margin: 30px auto 0;

            .specDiv {
                width: calc(100% / 4 - 30px);
                text-align: center;

                img {
                    max-width: 40%;
                }

                h3 {
                    margin-top: 10px;
                }
            }
        }
    }
}

</style>
