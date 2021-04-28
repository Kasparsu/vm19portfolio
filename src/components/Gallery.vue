<template>
    <div class="modal is-active">
        <div class="modal-background" @click="$emit('close')"></div>
        <div class="modal-content">
            <p class="image is-4by3">
                <img :src="images[current]" alt="">
            </p>
        </div>
        <div class="right" @click="right">
            <span class="icon is-large">
                <i class="fas fa-chevron-right fa-2x"></i>
            </span>
        </div>
        <div class="left" @click="left">
            <span class="icon is-large">
                <i class="fas fa-chevron-left fa-2x"></i>
            </span>
        </div>
        <button class="modal-close is-large" aria-label="close" @click="$emit('close')"></button>
    </div>
</template>

<script>
export default {
    props: ['images'],
    data() {
        return {
            current: 0
        }
    },
    methods: {
        left(){
            this.current++;
            if(this.current > this.images.length-1) {
                this.current = 0;
            }
        },
        right(){
            this.current--;
            if(this.current < 0) {
                this.current = this.images.length-1;
            }
        }
    }
}
</script>

<style scoped>
    .right {
        height: 100%;
        width: 10%;
        color:white;
        position: absolute;
        right:0;
        padding-top:50vh;
      
    }
    .left {
        height: 100%;
        width: 10%;
        color:white;
        position: absolute;
        left:0;
        padding-top:50vh;
        text-align: right;
    }
    .left:hover, .right:hover {
        background-color: rgba(0,0,0,0.5);
        
    }
</style>