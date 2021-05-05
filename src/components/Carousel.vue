<template>
<div>
  <div class="columns">
      
      <div class="column is-half" v-for="(review, index) in data" :key="index" :style="{'margin-left': !index ? -current*100 + '%' : 0}">
          <review-card :review="review"></review-card>
      </div>
  </div>
  <div class="carousel-pagination">
    <button v-for="i in data.length/2" :key="i" class="mr-1" @click="current=i-1" :class="{active: current===i-1}"></button>

  </div>
  </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue'
export default {
  components: { ReviewCard },
  mounted() {
    setInterval(()=> {
        this.current++;
        if(this.current>=this.data.length/2){
            this.current=0;
        }
    }, 10000);  
  },
  props: ['data'],
  data(){
      return {
          current: 0,
      }
  } 
}
</script>

<style scoped>
    .columns {
        max-width: 100%;
        overflow: hidden;
        margin-left: 0;
    }
    .column {
        transition: margin-left 0.2s linear;
    }
    .carousel-pagination {
        text-align: center;
    }
    .carousel-pagination button {
        background-color: white;
        border-color:orangered;
        border-style:solid;
        border-radius: 30%;
    }
    .carousel-pagination button.active {
        background-color: orangered;

    }
</style>