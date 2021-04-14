<template>
  <div>
    <my-header></my-header>
    <about></about>
    <intrests></intrests>
    <counters></counters>
    <offers><offers>
  </div>
</template>

<script>
import About from './components/About.vue';
import Counters from './components/Counters.vue';
import Intrests from './components/Intrests.vue';
import MyHeader from './components/MyHeader.vue';
import Offers from './components/Offers.vue';
export default {
  components: { MyHeader, About, Intrests, Counters, Offers },

}
</script>

<style>

</style>