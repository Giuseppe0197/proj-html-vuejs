<template>
    <div class="infoFooter">

        <ul class="about">
            <li class="title">{{details.titleAbout}}</li>
            <li class="borderBottom"></li>
            <li class="par">{{details.creation}}</li>
            <li><i class="icon" :class="details.linkedin"></i> <i class="icon" :class="details.facebook"></i> <i class="icon" :class="details.twitter"></i></li>
        </ul>

    </div>
</template>

<script>

export default {
  name: 'MyFooterSub',
  props: {
      details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    

.about {
    padding-top: 100px;
    width: 100%;

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
}

.borderBottom {
    border-bottom: 2px solid #ff4612;
    width: 50px;
}

.icon {
    color: white;
    margin-right: 10px;
    font-size: 23px;
}

.icon:hover {
    color: #ff4612;
    cursor: pointer;
}
</style>
