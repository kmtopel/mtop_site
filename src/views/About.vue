<template>
  <b-row class="about">  
    <h5>Our Vision</h5>
    <p>A world/community prepared to prevent exposure to trauma and minimize the adverse impact for those affected.</p>

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

export default {
  name:'about',
  components: {
    ListItem,
  }  
}
</script>

<style scoped>
ul {
  list-style-type: none;
}

</style>