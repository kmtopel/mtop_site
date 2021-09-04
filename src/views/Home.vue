<template>
<div>
  <b-row class='home'>
    <!-- <Banner title="Welcome!" bodyText='The Milwaukee Trauma Outcomes Project (MTOP) is a consortium dedicated to improving the lives of those affected by trauma through research, intervention, prevention, education, and outreach.'/> -->
  </b-row>
  <b-row>
    <b-col cols=1></b-col>
    <b-col cols=10>
      <Carousel />
    </b-col>
    <b-col cols=1></b-col>
  </b-row>
</div>
</template>

<script>
// import Banner from '@/components/Banner'
import Carousel from '@/components/Carousel'

export default {
  name: 'Home',
  components: {
    // Banner,
    Carousel,
  },
  data () {
    return {

    }
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
