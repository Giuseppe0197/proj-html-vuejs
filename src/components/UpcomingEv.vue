<template>
    <div class="events">
        <div class="container">
            <div class="upcoming">
                <div class="titleUp">
                    <h2>Upcoming Events</h2>
                </div>
                <div class="coaching">
                    <div class="calendar">
                        <h3>07</h3>
                        <p>Jan. 2022</p>
                    </div>

                    <div class="infos">
                        <h2>Melbourne Coaching</h2>
                        <p class="hour"><i class="far fa-clock"></i><span>9:00 am - 5:00 pm, Jan 7, 2022</span></p>
                        <p class="location"><i class="fas fa-map-marker-alt"></i><span>Cambridge, MA 02138, USA</span></p>
                        <p class="read">Read More</p>
                    </div>
                </div>

                <div class="coaching">
                    <div class="calendar">
                        <h3>11</h3>
                        <p>Jan. 2022</p>
                    </div>

                    <div class="infos">
                        <h2>New York Coaching</h2>
                        <p class="hour"><i class="far fa-clock"></i><span>9:00 am - 5:00 pm, Jan 11, 2022</span></p>
                        <p class="location"><i class="fas fa-map-marker-alt"></i><span>Cambridge, MA 02138, USA</span></p>
                        <p class="read">Read More</p>
                    </div>
                </div>

                <div class="coaching">
                    <div class="calendar">
                        <h3>21</h3>
                        <p>Jan. 2022</p>
                    </div>

                    <div class="infos">
                        <h2>London Coaching</h2>
                        <p class="hour"><i class="far fa-clock"></i><span>9:00 am - 5:00 pm, Jan 21, 2022</span></p>
                        <p class="location"><i class="fas fa-map-marker-alt"></i><span>Cambridge, MA 02138, USA</span></p>
                        <p class="read">Read More</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'UpcomingEv',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.events {
    background-image: url("../assets/img/h1-img-09.jpg");
    margin-top: 70px;
    height: 750px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    .container {
        position: relative;
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
