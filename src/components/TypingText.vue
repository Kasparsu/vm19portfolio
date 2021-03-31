<template>
  <h1>I am <span>{{ words[current].substr(0, length) }}</span><i class="blinker">|</i></h1>
</template>

<script>
export default {
    mounted(){
        setInterval(()=>{
            if(this.length === this.words[this.current].length){
                this.current++;
                if(this.current === this.words.length){
                    this.current = 0;
                }
                this.length = 0;
            }
            this.length++;
        }, 200);
    },
    data(){
        return {
            words: ['Web Designer', 'Web Developer', 'Photographer'],
            length: 0,
            current: 0,
        }
    }
}
</script>

<style scoped>
    h1 {
        position: absolute;
        color:whitesmoke;
        font-size:xx-large;
        font-weight: bold;
        width: 100vw;
        text-align: center;
    }
    span {
        color: #e54b4b;
    }

    .blinker {
        animation: blinker 0.4s cubic-bezier(1, 0, 0, 1) infinite alternate;  
    }

    @keyframes blinker {
        to { opacity: 0; }
    }
</style>