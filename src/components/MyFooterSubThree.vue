<template>
    <div class="importantlinks">

        <ul class="links">
            <li class="title">{{details.titleLinks}}</li>
            <li class="borderBottom"></li>
            <li class="grey">{{details.aboutMe}}</li>
            <li class="grey">{{details.aboutUs}}</li>
            <li class="grey">{{details.language}}</li>
            <li class="grey">{{details.coach}}</li>
            <li class="grey">{{details.events}}</li>
            
        </ul>

    </div>
</template>

<script>

export default {
  name: 'MyFooterSubThree',
  props: {
      details: Object
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.importantlinks {
    padding-top: 100px;

    .links {
        list-style-type: none;
    }

    li {
        list-style-type: none;
        margin-bottom: 20px;
    }

    .title {
        color: white;
        font-size: 25px;
    }

    .borderBottom {
    border-bottom: 2px solid #ff4612;
    width: 50px;
}

.grey {
    color: #8B8A8A;
}
}

</style>
