<template>
  <div class="background">
      <div class="container">
        <div class="columns">
            <div class="column is-one-quarter">
                <counter icon="far fa-smile" count="1251" text="Happy Clients"></counter>
            </div>
            <div class="column is-one-quarter">
                <counter icon="fas fa-trophy" count="15" text="Awards Won"></counter>
            </div>
            <div class="column is-one-quarter">
                <counter icon="fas fa-mug-hot" count="3261" text="Cup of Coffee"></counter>
            </div>
            <div class="column is-one-quarter">
                <counter icon="fas fa-flag-checkered" count="36" text="Project Complete"></counter>
            </div>
        </div>
      </div>
  </div>
</template>

<script>
import Counter from './Counter.vue'
export default {
  components: { Counter },

}
</script>

<style scoped>
    div.background {
        background: url('http://shreethemes.in/cristino/layouts/images/bg-counter.jpg') center center;
        margin: 15px;
        border-radius: 15px;
    }
    .container {
        padding-top:50px;
        padding-bottom: 50px;
    }
</style>