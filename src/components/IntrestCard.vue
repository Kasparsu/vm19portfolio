<template>
    <div>
        <span class="icon is-large">
            <i :class="icon" aria-hidden="true"></i>
        </span>
        <p class="card-header-title">
        {{title}}
        </p>             
    </div>
</template>

<script>
export default {
    props: ['title', 'icon']
}
</script>

<style scoped>
    .card-header-title {
        border-left: 1px solid lightgray;
    }
    div {
        background: #f9fafd;
        display: flex;
        transition: all 200ms;
    }
    div:hover {
        background: white;
        -webkit-box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2); 
        box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2);
        margin-top: -5px;
    }
    div:hover>span.icon {
        color:tomato;
    }
</style>