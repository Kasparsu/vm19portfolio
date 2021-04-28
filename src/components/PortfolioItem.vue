<template>
<div class="card">
    <div class="card-image">
        <div class="img-bg has-text-centered">
            <button class="button is-rounded" @click="$emit('gallery', data.images)">
                <span class="icon">
                    <i class="fas fa-camera-retro"></i>
                </span>
            </button>
        </div>
        <figure class="image is-4by3">
            <img :src="data.images[0]" alt="Placeholder image">
        </figure>
        
    </div>
    <div class="card-content">
        <div class="content">
            <h4 class="is-size-5 has-text-centered is-capitalized">{{data.title}}</h4>
            <h5 class="is-size-6 has-text-centered is-capitalized">{{data.tags[0]}}</h5>
        </div>
    </div>
</div>
</template>

<script>
export default {
    props: ['data']
}
</script>

<style scoped>
    .card {
        transition: all 200ms;
    }
    .card:hover {
        -webkit-box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2); 
        box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2);
        margin-top: -5px;
    }
    .img-bg {
        background-color: rgba(60,72,88,0.7);
        opacity: 0;
        height: 100%;
        position: absolute;
        width: 100%;
        z-index: 1;
        padding-top:50%;
        transition: all 200ms;
    }
    .img-bg button {
        background-color: rgba(60,72,88);
        color: white;
    }
    .img-bg button:hover {
        background-color: whitesmoke;
        color: orangered;
    }
    .card:hover .img-bg {
        opacity: 1;
        padding-top:25%
    }

</style>