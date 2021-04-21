<template>
  <section class="section">
      <div class="container">
          <heading title="Work Participation">
              Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.
          </heading>
        <timeline :data="timeline"></timeline>
      </div>
  </section>
</template>

<script>
import Heading from './Heading.vue'
import Timeline from './Timeline.vue'
export default {
  components: { Heading, Timeline },
  data(){
    return {
      timeline: [
        {from: 2015, to: 2018, proffession: 'UX Designer', firm:'Vivo - Senior Designer', description: 'The generated injected humour, or non-characteristic words etc. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis,'},
        {from: 2012, to: 2015, proffession: 'Web Developer', firm:'Oppo - HR Manager', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lacinia magna vel molestie faucibus. Donec auctor et urnaLorem ipsum dolor sit amet.'},
        {from: 2012 , to: 2010, proffession: 'Graphic Designer', firm:'Apple - Testor', description: 'Therefore always free from repetition, injected humour, or non-characteristic words etc. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis,'}
      ]
    }
  }
}
</script>

<style>

</style>