<template>
    <div class="contact">

        <ul class="contactLinks">
            <li class="title">{{details.titleContact}}</li>
            <li class="borderBottom"></li>
            <li class="grey"><i :class="details.addressIcon"></i>{{details.address}}</li>
            <li class="grey"><i :class="details.phoneIcon"></i>{{details.phone}}</li>
            <li class="grey"><i :class="details.mailIcon"></i>{{details.mail}}</li>
        </ul>

        <div class="form">
            <span>Your Name</span>

            <span id="subscribe">Subscribe</span>
        </div>

    </div>
</template>

<script>

export default {
  name: 'MyFooterSubFour',
  props: {
      details: Object
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .contact {
        padding-top: 100px;

        li {
            list-style-type: none;
            margin-bottom: 20px;
        }

        .borderBottom {
            border-bottom: 2px solid #ff4612;
            width: 50px;
        }

        .fas {
            color: #ff4612;
            margin-right: 20px;
        }

        .far {
            color: #ff4612;
            margin-right: 20px;
        }

        .title {
        color: white;
        font-size: 25px;
    }

    .grey {
    color: #8B8A8A;
}
    }

    .form {
        margin-top: 70px;
        border-bottom: 2px solid #8B8A8A;

        span {
            color: #8B8A8A;
        }
    }

    #subscribe {
        float: right;
        text-transform: uppercase;
        color: white;
        
    }
</style>
