<template>
  <section class="section">
      <heading title="Hobbies & Intrests">Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.</heading>
    <div class="container mt-6">
        <div class="columns is-multiline">
            <div class="column is-one-quarter" v-for="(intrest, index) in intrests" :key="index">
                <intrest-card :icon="intrest.icon" :title="intrest.title"><intrest-card>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import Heading from './Heading.vue'
import IntrestCard from './IntrestCard.vue'
export default {
  components: { Heading, IntrestCard },
  data(){
      return {
          intrests: [
              {icon: 'fas fa-laptop-code', title:'Developing'},
              {icon: 'fab fa-apple', title:'Mac OS'},
              {icon: 'fas fa-film', title:'Cinema'},
              {icon: 'fas fa-mug-hot', title:'Coffee'},
              {icon: 'fas fa-headphones-alt', title:'Music'},
              {icon: 'fas fa-gamepad', title:'Games'},
              {icon: 'fas fa-marker', title:'Designing'},
              {icon: 'fas fa-futbol', title:'Sports'},
              {icon: 'fas fa-paint-brush', title:'Painting'},
              {icon: 'fas fa-book-reader', title:'Reading'},
              {icon: 'fab fa-android', title:'Android'},
              {icon: 'fas fa-icons', title:'Other Activities'},
              
          ]
      }
  }
}
</script>

<style scoped>

</style>