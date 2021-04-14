<template>
  <div>
      <span class="icon is-large">
        <i class="fa-2x" :class="icon"></i>
      </span>
      <h1 class="is-size-3">{{count}}</h1>
      <h2 class="is-size-5">{{text}}</h2>
  </div>
</template>

<script>
export default {
    props: ['icon', 'count', 'text']
}
</script>

<style scoped>
    div {
        text-align: center;
    }
    .icon {
        color: orangered;
    }
    h1,h2 {
        color:white;
    }
</style>