<template>
    <div class="px-6 py-6 has-text-centered">
        <span class="icon is-large">
            <i class="fa-2x" :class="icon"></i>
        </span>
        <h1 class="is-size-3 is-capitalized">{{title}}</h1>
        <h2 class="is-size-6">{{text}}</h2>
        <h2 class="is-size-6 is-main"><a class="is-main" :href="dataLink">{{data}}</a></h2>
    </div>
</template>

<script>
export default {
    props: ['icon', 'title', 'text', 'data', 'data-link']
}
</script>

<style scoped>
.is-main {
    color: orangered;
}

</style>