<template>
  <div class="full-container pb-6 mb-6">
    <div class="img-wrapper2">
      <div class="img-wrapper">
        <img class="bg-img" src="http://shreethemes.in/cristino/layouts/images/home/02.jpg">
      </div>
    </div>
    <canvas ref="canvas" class="overlay"></canvas>
    <my-nav></my-nav>
    <section class="section is-medium">
      <div id="avatar" class="is-center mt-6">
        <figure class="image is-square">
          <img class="is-rounded" src="http://shreethemes.in/cristino/layouts/images/home/hero.jpg">
        </figure>
      </div>
           <typing-text></typing-text>
           <div class="article">

          <article>Obviously I'm a Web Designer. Web Developer with over 3 years of experience. Experienced with all stages of the development cycle for dynamic web projects.
            <button class="button cv-button mt-4">Download Cv</button>
          </article>
           
           </div>
           
    </section>
         
  </div>
</template>

<script>
import MyNav from './MyNav.vue'
import TypingText from './TypingText.vue'
export default {
  components: { MyNav, TypingText },
  mounted(){
    let el = this.$refs['canvas'];
    el.width = window.innerWidth;
    el.height = window.innerHeight;
    let ctx = el.getContext('2d');

    let orbs = [];
    for(let i = 0; i<300; i++){
        let x = Math.floor(Math.random() *el.width);
        let y = Math.floor(Math.random() *el.height);
        let angle = Math.floor(Math.random() *360);
        orbs.push({x: x, y:y, angle: angle})
    }
    setInterval(()=> {

        ctx.clearRect(0,0, el.width, el.height);
        orbs.forEach((orb) => {
            ctx.beginPath();
            ctx.arc(orb.x, orb.y, 5, 0, 2 * Math.PI);
            orb.x += Math.cos(this.deg2rad(orb.angle));
            orb.y += Math.sin(this.deg2rad(orb.angle));
            ctx.fillStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.fill();
            ctx.closePath();
            if(orb.x <0 || orb.y < 0 || orb.x > el.width || orb.y > el.height) {
                orb.angle += 90;
                orb.angle %= 360;
            }
            orbs.forEach((other)=> {
                // c2 = a2 + b2
                let dist = Math.sqrt(Math.pow(orb.x - other.x, 2) + Math.pow(orb.y - other.y, 2));
                if(dist < 100){
                    ctx.beginPath();
                    ctx.moveTo(orb.x, orb.y);
                    ctx.lineTo(other.x, other.y);
                    ctx.strokeStyle = 'rgba(255, 255, 255, '+ (1 - (dist / 100).toFixed(2)) +')';
                    ctx.stroke();
                    ctx.closePath();
                }
            });
        });

    }, 16)
  },
  methods: {
    deg2rad(deg){
        return deg * (Math.PI / 180);
    },
    rad2deg(rad){
        return rad * (180/ Math.PI);
    }
  }
}
</script>

<style>
  .bg-img {
    margin-top: -200px;
  }
  .img-wrapper {
    height: 900px;
    overflow: hidden;
    position: absolute;
  }
  .img-wrapper2 {
    position: relative;
  }
  .overlay {
    background-color: rgba(60,72,88,0.7);
    height: 900px;
    position: absolute;
    width:100%;

  }
  #avatar {
    width: 190px;
    height: 190px;
  
  }
  #avatar>figure>img {
    border: lightgray solid 5px;
  }
  article {
    color: darkgray;

    width:600px;
    text-align: center;
    margin: 0 auto;
        margin-top:50px;
        font-weight: bold;

  }
  .article {
    position: relative;
    width: 100vw;
  }
  .cv-button {
    margin: 0 auto;
    background-color: #e54b4b; 
    border-color: #e54b4b;
    color: whitesmoke;
  }
</style>