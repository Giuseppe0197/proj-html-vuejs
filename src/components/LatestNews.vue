<template>
<div class="news">

    <div class="latest">
        <img id="imageBack" src="../assets/img/svg-4.svg" alt="">

        <div class="titleNews">
            <h2>Latest news<span class="dot">.</span></h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            <div class="borderbottom"></div>

        </div>

        <img class="arrowleft" src="../assets/img/svg-6.svg" alt="">

        <img class="arrowright" src="../assets/img/svg-6.svg" alt="">

        <button class="buttonLatest"><i class="fas fa-long-arrow-alt-up"></i></button>
    </div>

    <div class="imageInfo">
        

        <div class="imagesNews" v-for="news, i in newsList" :key="i">
            <div class="image">
                <img :src="require(`../assets/img/${news.image}`)" alt="">
            </div>
            <i class="far fa-clock"></i><span>{{news.date}}</span>
            <i class="far fa-user"></i><span>{{news.name}}</span>
            <h3>{{news.titleNews}}</h3>
            <p>{{news.paragraph}}</p>
            <h5>{{news.read}}</h5>
        </div>

        
    </div>

</div>
</template>

<script>
export default {
  name: 'LatestNews',

  data() {
      return {
          newsList: [
            {
            'image': 'h1-blog-img-02.jpg',
            'date': 'May 5, 2019',
            'name': 'Amanda Doe',
            'titleNews': 'Next investment',
            'paragraph': 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium necessitatibus nisi sequi',
            'read': 'read more'
            },

            {
            'image': 'h1-blog-img-03.jpg',
            'date': 'May 5, 2019',
            'name': 'Amanda Doe',
            'titleNews': 'Team Building',
            'paragraph': 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium necessitatibus nisi sequi',
            'read': 'read more'
            },

            {
            'image': 'h1-blog-img-04.jpg',
            'date': 'May 5, 2019',
            'name': 'Amanda Doe',
            'titleNews': 'New Business Day',
            'paragraph': 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium necessitatibus nisi sequi',
            'read': 'read more'
            }
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.news {
    

    .latest {
        position: relative;

        #imageBack {
            position: absolute;
            top: -80px;
            left: 150px;
            width: 20%;
        }

        .arrowleft {
            filter: invert(1);
            transform: rotate(180deg);
            position: absolute;
            left: 50px;
            top: 300px;
            cursor: pointer;
        }

        .arrowright {
            filter: invert(1);
            position: absolute;
            right: 70px;
            top: 300px;
            cursor: pointer;
        }

        .buttonLatest {
                background-color: white;
                border: none;
                border-radius: 50%;
                padding: 10px 15px;
                position:absolute;
                right: 20px;
                bottom: -120px;
            }

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }

        .titleNews {
            text-align: center;
            margin-top: 50px;

            .dot {
                color: #ff4612;
            }

            h2 {
                font-size: 40px;
            }

            p {
                margin: 20px 0;
                color: #B2B2B2;
            }

            .borderbottom {
                border-bottom: 2px solid #ff4612;
                width: 5%;
                margin: 0 auto;
            }

        }

    }

    .imageInfo {
        width: 90%;
        margin: 70px auto;
        display: flex;
        justify-content: center;

    }

    .imagesNews {
        width: calc(100% / 4 - 30px);
        margin-right: 30px;
        z-index: 99;

        img {
            max-width: 100%;
            margin-bottom: 20px;
        }

        .far {
            color: #ff4612;
            font-size: 12px;
            margin-right: 10px;
        }

        span {
            font-size: 12px;
            margin-right: 5px;
        }


        h3 {
            margin: 10px 0;
            font-size: 22px;
        }

        p {
            margin-bottom: 10px;
            font-size: 13px;
            color: #B2B2B2;
        }

        h5 {
            text-transform: uppercase;
            margin: 10px 0 100px;
        }
    }
}
</style>
