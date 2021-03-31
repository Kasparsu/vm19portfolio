<template>
  <div class="full-container">
    <div class="img-wrapper">
      <img class="bg-img" src="http://shreethemes.in/cristino/layouts/images/home/02.jpg">
    </div>
    <div class="overlay"></div>
    <my-nav></my-nav>
    <section class="section">
      <div id="avatar" class="is-center">
        <figure class="image is-square">
          <img class="is-rounded" src="http://shreethemes.in/cristino/layouts/images/home/hero.jpg">
        </figure>
      </div>
    </section>
  </div>
</template>

<script>
import MyNav from './MyNav.vue'
export default {
  components: { MyNav },
}
</script>

<style>
  .bg-img {
    margin-top: -200px;
  }
  .img-wrapper {
    height: 900px;
    overflow: hidden;
    position: absolute;
  }
  .overlay {
    background-color: rgba(60,72,88,0.7);
    height: 900px;
    position: absolute;
    width:100%;

  }
  #avatar {
    width: 190px;
    height: 190px;
  
  }
  #avatar>figure>img {
    border: lightgray solid 5px;
  }
</style>