<template>
    <div class="infoFooterTwo">

        <ul class="links">
            <li class="title">{{details.titleTwitter}}</li>
            <li class="borderBottom"></li>
            <li class="par"><i :class="details.twitterPar"></i><a href="">{{details.adam}}</a> {{details.hello}} <a href="">{{details.adam}}</a> {{details.submit}} <a href="">{{details.linkSubmit}}</a> {{details.submitTwo}} <a href="">{{details.linkSupport}}</a></li>
            <li class="par"><i :class="details.twitterPar"></i><a href="">{{details.henry}}</a> {{details.checkOut}} <a href="">{{details.linkMarket}}</a></li>
        </ul>

    </div>
</template>

<script>

export default {
  name: 'MyFooteSubTwo',
  props: {
      details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.links {
    padding-top: 100px;

    li {
        list-style-type: none;
        margin-bottom: 20px;
    }

    .title {
        color: white;
        font-size: 25px;
    }

    .par {
        color: #8B8A8A;
    }

    a {
        color: #8B8A8A;
    }

    .fa-twitter {
        color: #ff4612;
        margin-right: 20px;
    }

    .borderBottom {
    border-bottom: 2px solid #ff4612;
    width: 50px;
}
}

</style>
