<template>
  <div>
       <label>
            {{title}}
        </label>
        <progress class="progress is-small" :value="current" max="100">{{value}}%</progress>
  </div>
</template>

<script>
export default {
    props: ['title', 'value'],
    mounted(){
        this.interval = setInterval(()=> {
            if(this.current<this.value){
                this.current++;
            } else {
                clearInterval(this.interval);
            }
        }, 10);
    },
    data(){
        return {
            current: 0,
            interval: null,
        }
    }
}
</script>

<style scoped>
    progress {
        fill: orangered;
    }
    progress::-webkit-progress-value { background: orangered; }
</style>