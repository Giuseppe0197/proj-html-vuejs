<template>
<div class="leader">
    <div class="creative">

        <!-- sezione con le info del leader -->

        <div class="leaderInfo">
            <h1>Creative Leader<span class="dot">.</span></h1>
            <div class="borderbottom">
            </div>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores, tempora asperiores veritatis cum incidunt sequi deleniti libero deserunt voluptates, repellendus eaque maxime alias beatae.</p>
            <h4>read more</h4>
        </div>

        <!-- div creati per la parte delle percentuali -->

        <div class="percentage">
            <div class="titleRequired">
                <h3>Mentorship</h3>
                <span class="numberPerc">78%</span>
            </div>

            <!-- div per la simulazione dei colori delle percentuali -->

            <div class="border">
            <div class="borderPerc1">
            </div>
            <div class="borderright1"></div>
            </div>

            <div class="titleRequired">
                <h3>Education</h3>
                <span class="numberPerc">95%</span>
            </div>

            <!-- div per la simulazione dei colori delle percentuali -->

            <div class="border">
            <div class="borderPerc2">
            </div>
            <div class="borderright2"></div>
            </div>

            <div class="titleRequired">
                <h3>Learning</h3>
                <span class="numberPerc">65%</span>
            </div>
            <!-- div per la simulazione dei colori delle percentuali -->

            <div class="border">
            <div class="borderPerc3">
            </div>
            <div class="borderright3"></div>
            </div>

            <div class="titleRequired">
                <h3>Motivation</h3>
                <span class="numberPerc">83%</span>
            </div>
            <!-- div per la simulazione dei colori delle percentuali -->
            
            <div class="border">
            <div class="borderPerc4">
            </div>
            <div class="borderright4"></div>
            </div>
        </div>
        
    </div>
</div>
</template>

<script>
export default {
  name: 'Leader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.leader {
    background-color: white;
    height: 400px;

    .creative {
        width: 75%;
        margin: 0 auto;
        padding-top: 80px;
        display: flex;
        

        .leaderInfo {
            width: 50%;

            .dot {
                color: #ff4612;
            }

            .borderbottom{
                border-bottom: 2px solid #ff4612;
                width: 50px;
                margin: 30px 0;
            }

            p {
                color: #B2B2B2;
                margin-bottom: 10px;
                line-height: 22px;
            }

            h4 {
                text-transform: uppercase;
            }

        }
        /* creiamo dei div per le percentuali */

        .percentage {
            width: 40%;
            
            .titleRequired {
                display: flex;
                justify-content: space-between;
            } 
        }

        .border {
            display: flex;
            /* creiamo div per simulare la barra colorata fino alla determinata percentuale */

        .borderPerc1 {
            border-bottom: 3px solid #ff4612;
            width: 78%;
            margin: 10px 0 25px 0;
        }
        .borderright1 {
            border-bottom: 1px solid grey;
            width: 22%;
            margin: 10px 0 25px 0;
        }

        .borderPerc2 {
            border-bottom: 3px solid #ff4612;
            width: 95%;
            margin: 10px 0 25px 0;;
        }

        .borderright2 {
            border-bottom: 1px solid grey;
            width: 5%;
            margin: 10px 0 25px 0;
        }

        .borderPerc3 {
            border-bottom: 3px solid #ff4612;
            width: 65%;
            margin: 10px 0 25px 0;;
        }

        .borderright3 {
            border-bottom: 1px solid grey;
            width: 35%;
            margin: 10px 0 25px 0;
        }

        .borderPerc4 {
            border-bottom: 3px solid #ff4612;
            width: 83%;
            margin: 10px 0 25px 0;;
        }

        .borderright4 {
            border-bottom: 1px solid grey;
            width: 17%;
            margin: 10px 0 25px 0;
        }

    }


    }
}
</style>
