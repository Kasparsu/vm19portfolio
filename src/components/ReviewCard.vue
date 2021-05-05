<template>
  <div class="box">
        <div>
            <span class="icon is-small">
                <i class="fas fa-star"></i>
            </span>
            <span class="icon is-small">
                <i class="fas fa-star"></i>
            </span>
            <span class="icon is-small">
                <i class="fas fa-star"></i>
            </span>
            <span class="icon is-small">
                <i class="fas fa-star"></i>
            </span>
            <span class="icon is-small">
                <i class="fas fa-star"></i>
            </span>
        </div>
        <h5 class="is-size-5"><b>" {{review.quote}} "</b></h5>
        <p>{{review.text}}</p>
        <div class="media">
            <div class="media-left">
                <figure class="image is-48x48">
                    <img class="is-rounded" :src="review.image" alt="Placeholder image">
                </figure>
            </div>
            <div class="media-content">
                <p class="title is-4">{{review.name}}</p>
                <p class="subtitle is-6">{{review.organisation}}</p>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    props:['review']
}
</script>

<style scoped>
.icon {
    color: orangered;
}
</style>