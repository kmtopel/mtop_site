<template>
<b-jumbotron fluid class='banner' bg-variant="light">
    <h5>{{title}}</h5>
    <p class='bodyText' >{{ bodyText }}</p>
    <b-img :src='image'></b-img>
    <b-button variant="light" to="/about">Learn More</b-button>
</b-jumbotron>
</template>

<script>
export default {
    name: 'Banner',
    props: {
        title: String,
        bodyText: String,
        image: String,
    },
  
}
</script>

<style scoped>
.banner {
    width: 100%;    
}
</style>