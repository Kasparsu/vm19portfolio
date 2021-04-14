<template>
  <div class="wrapper">
      <div class="px-6 py-6">
        <span class="icon is-large">
            <i class="fa-2x" :class="icon"></i>
        </span>
        <h1 class="is-size-3">{{title}}</h1>
        <h2 class="is-size-6">{{text}}</h2>
        <span class="icon background">
            <i :class="icon"></i>
        </span>
        
    </div>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
    props: ['icon', 'title', 'text']
}
</script>

<style scoped>
    .wrapper {
        text-align: center;
        border: 1px solid lightgray;
        border-radius: 10px;
        transition: all 200ms;
        
    }
    .wrapper:hover {
        background: white;
        -webkit-box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2); 
        box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2);
        margin-top: -5px;
    }
    .background {
        float: right;
    }
    .line {
        height: 3px;
        width: 0%;
        border-bottom: 3px orangered solid;
        transition: all 200ms;
        margin:0 auto;
    }
    .wrapper:hover>.line {
        width: 100%;
    }
    .wrapper:hover>div>.background {
        margin-top: -200px;
        margin-right: 200px;
        transition: all 200ms;
    }
    .wrapper:hover>div>h1 {
        color:orangered;
    }
    .wrapper:hover>div>.background>i::before {
        font-size: 200px;
        opacity: 20%;
        transition: all 200ms;
    }
    .background {
        transition: all 200ms;
    }
    .background>i::before {
        font-size: 40px;
        color:orangered;
        position: absolute;
        z-index: 0;
        opacity: 5%;
        transition: all 200ms;
    }
    .icon {
        color: orangered;
    }
</style>