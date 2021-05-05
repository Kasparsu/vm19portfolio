<template>
  <div>
    <my-header></my-header>
    <about></about>
    <intrests></intrests>
    <counters></counters>
    <offers></offers>
    <work-participation></work-participation>
    
    <expertise></expertise>
    <portfolio></portfolio>
    <reviews></reviews>
    <blog-posts></blog-posts>
  </div>
</template>

<script>
import About from './components/About.vue';
import BlogPosts from './components/BlogPosts.vue';
import Counters from './components/Counters.vue';
import Expertise from './components/Expertise.vue';
import Intrests from './components/Intrests.vue';
import MyHeader from './components/MyHeader.vue';
import Offers from './components/Offers.vue';
import Portfolio from './components/Portfolio.vue';
import Reviews from './components/Reviews.vue';
import WorkParticipation from './components/WorkParticipation.vue';
export default {
  components: { MyHeader, About, Intrests, Counters, Offers, WorkParticipation, Expertise, Portfolio, Reviews, BlogPosts },

}
</script>

<style>

</style>