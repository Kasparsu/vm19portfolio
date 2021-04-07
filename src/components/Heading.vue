<template>
    <div>
        <article>
            <h1 class="is-size-3"><b>{{title}}</b></h1>
            <slot></slot>
        </article>
    </div>
</template>

<script>
export default {
    props: ['title']
}
</script>

<style>
    
    h1 {
        border-bottom: 1px solid tomato;
        text-transform: uppercase;
    }
</style>