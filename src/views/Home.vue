<template>
<div class='home'>
    <b-jumbotron lead="Welcome!" bg-variant="light">
    <p class='bodyText' >The Milwaukee Trauma Outcomes Project (MTOP) is a consortium dedicated to improving the lives of those affected by trauma through research, intervention, prevention, education, and outreach.</p>
    <b-button  variant="light" to="/about">Learn More</b-button>
  </b-jumbotron>
    
</div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style scoped>
.bodyText {
  text-align: left;
  padding: 35px;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
