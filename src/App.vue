<template>
  <div>
    <my-header></my-header>
    <about></about>
    <intrests></intrests>
  </div>
</template>

<script>
import About from './components/About.vue';
import Intrests from './components/Intrests.vue';
import MyHeader from './components/MyHeader.vue';
export default {
  components: { MyHeader, About, Intrests },

}
</script>

<style>

</style>