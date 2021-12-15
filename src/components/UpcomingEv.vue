<template>

<!-- creiamo una sezione per gli eventi in arrivo -->
    <div class="events">
        <div class="container">
            <div class="upcoming">
                <div class="titleUp">
                    <h2>Upcoming Events</h2>
                </div>

                 <!-- creiamo la sezione che conterrà le informazioni per gli eventi -->
                <div v-for="events, i in eventCity" :key="i" class="coaching">
                    <div class="calendar">
                        <h3>{{events.day}}</h3>
                        <p>{{events.year}}</p>
                    </div>

                    <div class="infos">
                        <h2>{{events.titleEvent}}</h2>
                        <p class="hour"><i :class="events.clock"></i><span>{{events.hour}}</span></p>
                        <p class="location"><i :class="events.where"></i><span>{{events.location}}</span></p>
                        <p class="read">{{events.readMore}}</p>
                    </div>
                </div>
            </div>
            <button class="buttonEvents"><i class="fas fa-long-arrow-alt-up"></i></button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'UpcomingEv',

  data () {
      return {
          eventCity: [
              {
                  'day': '07',
                  'year': 'Jan. 2022',
                  'titleEvent': 'Melbourne Coaching',
                  'clock': 'far fa-clock',
                  'hour': '9:00 am - 5:00 pm, Jan 7, 2022',
                  'where': 'fas fa-map-marker-alt',
                  'location': 'Cambridge, MA 02138, USA',
                  'readMore': 'Read More'
              },

              {
                  'day': '11',
                  'year': 'Jan. 2022',
                  'titleEvent': 'New York Coaching',
                  'clock': 'far fa-clock',
                  'hour': '9:00 am - 5:00 pm, Jan 7, 2022',
                  'where': 'fas fa-map-marker-alt',
                  'location': 'Cambridge, MA 02138, USA',
                  'readMore': 'Read More'
              },

              {
                  'day': '21',
                  'year': 'Jan. 2022',
                  'titleEvent': 'London Coaching',
                  'clock': 'far fa-clock',
                  'hour': '9:00 am - 5:00 pm, Jan 7, 2022',
                  'where': 'fas fa-map-marker-alt',
                  'location': 'Cambridge, MA 02138, USA',
                  'readMore': 'Read More'
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

/* stilizziamo le varie sezioni */
.events {
    background-image: url("../assets/img/h1-img-09.jpg");
    margin-top: 70px;
    height: 750px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    .container {
        position: relative;

        .buttonEvents {
                background-color: white;
                border: none;
                border-radius: 50%;
                padding: 10px 15px;
                position:absolute;
                right: 20px;
                top: 350px;
            }

            .fa-long-arrow-alt-up {
                color: #ff4612;
                font-size: 18px;
            }
    }

    .upcoming {
        width: 30%;
        background-color: white;
        /* height: 300px; */
        position: absolute;
        left: 200px;
        top: 120px;
        background-color: #FAFAFA;
    }

    .titleUp {
        height: 70px;
        box-shadow: 0 0 15px grey;

        h2 {
            margin-left: 25px;
            padding-top: 10px;
        }
    }
     .coaching:hover{
         background-color: white;
         cursor: pointer;
     }

    .coaching {
        border-bottom: 1px solid rgb(197, 197, 197);
        display: flex;

        .calendar {
            background-color: #ff4612;
            height: 60px;
            width: 15%;
            color: white;
            text-align: center;
            padding: 10px;
            margin: 20px;

            p {
                font-size: 10px;
            }
        }

        .infos {
            margin: 20px 0;

            .hour {
                margin: 10px 0;
            }

            .location {
                margin-bottom: 10px;
            }

            .fa-clock {
                color: #ff4612;
                margin-right: 10px;
            }

            .fa-map-marker-alt {
                color: #ff4612;
                margin-right: 10px;
            }

            p {
                font-size: 10px;
                color: grey;
            }

            .read {
                color: black;
                text-transform: uppercase;
                font-weight: bold;
            }
            
        }
    }
}
</style>
