<template>
  <b-row class="about">
    <!-- <Banner :showBtn='false' bodyText='MTOP was founded around a group of researchers from the Medical College of Wisconsin, University of Wisconsin-Milwaukee, Marquette University, and the Milwaukee VA. This team’s expertise spans neurobiological, cognitive, behavioral, social, and intervention science. The current core membership provides a strong foundation in neurobiological and psychological mechanisms that predict risk and resilience in the aftermath of trauma, validated interventions for post traumatic stress, socio-environmental influences on trauma outcomes, and affect dysregulation in post traumatic stress conditions.' />     -->
    <h5>Our Vision</h5>
    <ul>
      <ListItem
      text='A world/community prepared to prevent exposure to trauma and minimize the adverse impact for those affected.'
      />
    </ul>
    <h5 >Our Mission</h5>
    <ul>
      <ListItem 
      title='Markers & Mechanisms' 
      text='To advance understanding of factors that foster risk or resilience for posttraumatic stress and other problems following trauma exposure' 
      />
      <ListItem 
      title='Intervention' 
      text='To empirically validate and implement novel treatments for trauma survivors and increase precision of matching interventions with patients and with specific symptom profiles'
      />
      <ListItem 
      title='Prevention' 
      text='To empirically validate and implement approaches to minimize risk for PTSD in at-risk acute trauma survivors'
      />
      <ListItem 
      title='Community Engagement' 
      text='To maximize the utility of these research efforts via direct input into clinically meaningful outcomes and research approaches from providers, community agencies serving trauma-exposed individuals, and trauma-exposed individuals and communities themselves'
      />
      <ListItem 
      title='Education and Training' 
      text='To disseminate research findings directly to Milwaukee area providers and agencies to advance front-line care, to educate providers in specific techniques for assessing risk and offering prevention and intervention approaches, and to educate the public and policy makers about risk factors and opportunities for prevention and intervention'
      />
      <ListItem 
      title='Community Engagement/Population Health' 
      text='To provide a forum for a network of scientists, providers, and communities to share their unique perspectives on trauma and trauma-informed care and to work together to improve quality of life for trauma survivors and trauma-impacted communities'
      />
    </ul>
  </b-row>
</template>

<script>
import ListItem from '@/components/ListItem'
// import Banner from '@/components/Banner'

export default {
  name:'about',
  components: {
    ListItem
    // Banner
  }  
}
</script>

<style scoped>
ul {
  list-style-type: none;
}

</style>