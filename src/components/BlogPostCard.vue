<template>
  <div class="card">
    <div class="card-image">
        <figure class="image is-4by3">
            <img :src="data.image" alt="Placeholder image">
        </figure>
        
    </div>
    <div class="card-content">
        <div class="content">
            <div>
                <span class="icon-text">
                    <span class="icon">
                        <i class="fas fa-user"></i>
                    </span>
                    <span>{{data.user}}</span>
                </span>
                <span class="icon-text is-pulled-right">
                    <span class="icon">
                        <i class="fas fa-tag"></i>
                    </span>
                    <span>{{data.tag}}</span>
                </span>
            </div>
            <h4 class="is-size-5  is-capitalized">{{data.title}}</h4>
            
        </div>
    </div>
    <footer class="card-footer is-block py-3 px-3">

        <a href="#" class="is-size-6"><b>Read more</b> 
            <span class="icon">
                <i class="fas fa-chevron-right"></i>
            </span>
        </a>
        <span class="icon-text is-pulled-right">
            <span class="icon">
                <i class="fas fa-calendar"></i>
            </span>
            <span>{{data.created}}</span>
        </span>
  </footer>
</div>
</template>

<script>
export default {
    props: ['data']
}
</script>

<style>
    .card {
        transition: all 200ms;
    }
    .card:hover {
        -webkit-box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2); 
        box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2);
        margin-top: -5px;
    }
</style>