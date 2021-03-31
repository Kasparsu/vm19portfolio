<template>
  <div class="full-container">
    <div class="img-wrapper2">
      <div class="img-wrapper">
        <img class="bg-img" src="http://shreethemes.in/cristino/layouts/images/home/02.jpg">
      </div>
    </div>
    <div class="overlay"></div>
    <my-nav></my-nav>
    <section class="section is-medium">
      <div id="avatar" class="is-center mt-6">
        <figure class="image is-square">
          <img class="is-rounded" src="http://shreethemes.in/cristino/layouts/images/home/hero.jpg">
        </figure>
            <typing-text></typing-text>
      </div>
    </section>
         
  </div>
</template>

<script>
import MyNav from './MyNav.vue'
import TypingText from './TypingText.vue'
export default {
  components: { MyNav, TypingText },
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
  .img-wrapper2 {
    position: relative;
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