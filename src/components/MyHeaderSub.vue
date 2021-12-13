<template>
  <div class="subheader">

    <div class="headerlinks">

        <div class="logo">
            <img :src="require(`../assets/img/${details.image}`)">
        </div>

        <div class="menuEl">
            <ul>
                <li><img class="arrowImage" :src="require(`../assets/img/${details.imageArrow}`)"></li>
                <li class="home">{{details.home}}</li>
                <li>{{details.page}}</li>
                <li>{{details.blog}}</li>
                <li>{{details.shop}}</li>
                <li><i class="fas fa-search"></i></li>
                <li><i class="fas fa-bars"></i></li>
            </ul>
        </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'MyHeaderSub',
  props: {
      details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.headerlinks {
    display: flex;
    justify-content: space-between;
    width: 90%;
    margin: 0 auto;
    height: 100px;
}

.logo img {
    width: 50%;
    margin-top: 20px;
}

ul li{
    display: inline-block;
    margin-right: 20px;
    margin-top: 20px;
    vertical-align: middle;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 12px;
}

.home {
    color: #ff4612;
}

</style>
