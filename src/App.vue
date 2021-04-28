<template>
  <div>
    <my-header></my-header>
    <about></about>
    <intrests></intrests>
    <counters></counters>
    <offers></offers>
    <work-participation></work-participation>
    <expertise></expertise>
    <portfolio><portfolio>
  </div>
</template>

<script>
import About from './components/About.vue';
import Counters from './components/Counters.vue';
import Expertise from './components/Expertise.vue';
import Intrests from './components/Intrests.vue';
import MyHeader from './components/MyHeader.vue';
import Offers from './components/Offers.vue';
import Portfolio from './components/Portfolio.vue';
import WorkParticipation from './components/WorkParticipation.vue';
export default {
  components: { MyHeader, About, Intrests, Counters, Offers, WorkParticipation, Expertise, Portfolio },

}
</script>

<style>

</style>