<template>
  <section class="section">
      <span class="icon">
    <i class="far fa-star"></i>
  </span>
      <div class="columns is-multiline">
          <template v-for="(item,index) in data" >
            <div class="column is-half" :key="'date-' + index" v-if="index%2===0">
                <div class="box">
                    {{item.from}} - {{item.to}}
                    <div class="circle-wrapper">
                        <div class="circle"></div>
                    </div>
                </div>
            </div>
            <div class="column is-half" :key="'body-' + index">
                <div class="box body">
                <h4 class="is-size-5">{{item.proffession}}</h4>
                    <h5 class="is-size-6">{{item.firm}}</h5>
                    <p>
                        {{item.description}}
                    </p>
                </div>
            </div>
            <div class="column is-half" :key="'date-' + index" v-if="index%2===1">
                <div class="box">
                    {{item.from}} - {{item.to}}
                    <div class="circle-wrapper">
                        <div class="circle"></div>
                    </div>
                </div>
            </div>
          </template>
      </div>
  </section>
</template>

<script>
export default {
    props: ['data']
}
</script>

<style scoped>
    .column:nth-child(odd)>.box {
        float: right;
  
    }
    .column:nth-child(odd) {
        border-right: 2px solid lightgray;
    }
    .column:nth-child(even)>.box {
        float: left;
    }
    .circle {
        border: 3px solid black;
        border-radius: 10px;
        width: 15px;
        height: 15px;
        position:relative;
        bottom:15px;
        background: white;
    }
    .column:nth-child(odd)>.box .circle {
               left: 110px;
    }
    .column:nth-child(even)>.box .circle {
               right: 40px;
    }
    .column:nth-child(odd)>.box.body   {
              text-align: right;
    }
    .circle-wrapper {
        position:absolute;
    }
    .body {
        top: 0;
        position: relative;
        transition: all 200ms;
    }
    .body:hover {
        -webkit-box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2); 
        box-shadow: 0px 5px 20px 7px rgba(0,0,0,0.2);
        top: -10px;
    }
    .body:hover h4 {
        color: orangered;
    }

    .icon {
        position: relative;
        left: 50%;
    }
    .icon i {
        margin-right:25px;
        padding:5px;
        border: 2px solid lightgray;
        border-radius: 25px;
        background: white;
    }
</style>