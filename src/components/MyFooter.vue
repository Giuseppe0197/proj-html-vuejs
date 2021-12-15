<template>
    <footer>

        <div class="infos">

            <MyFooterSub class="compInfo"
            v-for="links, i in footerLinks"
            :key="i"
            :details="links"/>

            <MyFooteSubTwo class="compInfo"
            v-for="linksTwo, i in linkFooterTwo"
            :key="i"
            :details="linksTwo"/>

            <MyFooterSubThree class="compInfo"
            v-for="linksThree, i in importantLinks"
            :key="i"
            :details="linksThree"/>

            <MyFooterSubFour
            class="compInfo"
            v-for="contact, i in contactLinks"
            :key="i"
            :details="contact"/>

        </div>

        <div id="footerBottom">
            <span>Copyright Everlead &copy;MikadoThemes</span>
            <button class="buttonFooter"><i class="fas fa-long-arrow-alt-up"></i></button>
        </div>

        
    </footer>
</template>

<script>

import MyFooterSub from '@/components/MyFooterSub.vue'
import MyFooteSubTwo from '@/components/MyFooteSubTwo.vue'
import MyFooterSubThree from '@/components/MyFooterSubThree.vue'
import MyFooterSubFour from '@/components/MyFooterSubFour.vue'

export default {
  name: 'MyFooter',
  components: {
     MyFooterSub,
     MyFooteSubTwo,
     MyFooterSubThree,
     MyFooterSubFour
  },
  data() {
      return {
          footerLinks: [
            {
            'titleAbout': 'About',
            'creation': 'We created Everlead to effectively become the stepping stone towards meeting all your goals & achieving business success',
            'linkedin': 'fab fa-linkedin',
            'facebook': 'fab fa-facebook',
            'twitter': 'fab fa-twitter-square'
            },

          ],

          linkFooterTwo : [
            {
            'titleTwitter': 'Twitter',
            'twitterPar': 'fab fa-twitter',
            'adam': '@aliasadamd',
            'hello': 'Hi',
            'submit': ', can you please submit a ticket at',
            'submitTwo': ' and one of your support agent...',
            'linkSubmit': 'https://t.co/JLV61aXG7d',
            'linkSupport': 'https://t.co/yk57k1S9bS',
            'henry': '@HenrySefaBoakyl',
            'checkOut': 'Check out our theme Gioia which has all necessary elements to build a multi vendor marketplace.',
            'linkMarket': 'https://t.co/c9BIYxZBIL'
            },
          ],

          importantLinks: [

            {
            'titleLinks': 'Important Links',
            'aboutMe': 'About me',
            'aboutUs': 'About us',
            'language': 'Language packs',
            'coach': 'Become a coach',
            'events': 'Monthly events'
            },

          ],

           contactLinks: [

               {
               'titleContact': 'Contact me',
               'addressIcon': 'fas fa-map-marker-alt',
               'address': '457 BigBlue Street, NY 10013',
               'phoneIcon': 'fas fa-phone-alt',
               'phone': '(315) 5512-2579',
               'mailIcon': 'far fa-envelope',
               'mail': 'everlead@mikado.com',
               'yourName': 'Your Name',
               'subscribe': 'subscribe',
               },

           ]

      }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    footer {
        background-color: #181515;
        /* height: 500px; */

        .infos {
            width: 70%;
            margin: 0 auto;
            display: flex;
            justify-content: space-evenly;
        }

        .compInfo {
            width: calc(100% / 4 - 20px);
        }

        #footerBottom {
            background-color: #ff4612;
            text-align: center;
            height: 30px;
            vertical-align: middle;
            line-height: 30px;
            position: relative;
            margin-top: 100px;

            span {
                font-size: 12px;
                color: #8B8A8A;
            }

            .buttonFooter {
                background-color: white;
                border: none;
                border-radius: 50%;
                padding: 10px 15px;
                position:absolute;
                right: 20px;
                top: -20px;
            }

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }
        }
    }
</style>
