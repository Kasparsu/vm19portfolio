<template>
  <section class="section is-medium mt-6">
      <div class="columns">
        <div class="column is-one-quarter is-offset-one-quarter">
            <figure class="image" id="profile-pic">
                <img  src="http://shreethemes.in/cristino/layouts/images/hero.png">
            </figure>
        </div>
        <div class="column">
            <section class="section montserrat">
    
                    <h4 class="is-size-4 pb-4 is-main-color"><b>Cristino Murphy</b></h4>
                    <h5 class="is-size-5 pb-4">I'm a Passionate <span class="is-main-color">Web Designer</span></h5>
                    <div class="body">
                    Obviously I'm a Web Designer. Web Developer with over 3 years of experience. <br>
                    
                    Experienced with all stages of the development cycle for dynamic web projects. <br>
                    The as opposed to using 'Content here, content here', making it look like readable English.<br><br>

                    The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, <br>
                    as opposed to using 'Content here, content here', making it look like readable English.
                    </div>
                <div style="width:140px" class="py-4">
                    <figure class="image">
                        <img src="http://shreethemes.in/cristino/layouts/images/sign.png">
                    </figure>
                </div>
                <button class="button is-main">View Portfolio</button>
            </section>
        </div>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
    .montserrat {
        font-family: 'Montserrat', sans-serif;
        font-weight: 600;
    }
    h4 {
        font-weight: 600;
    }
    h5 {
        font-weight: 600;
    }
    .body {
        font-weight: normal;
        font-size: medium;
        color:darkgray;
    }
    #profile-pic::before {
        content: '';
        border: 20px solid lightgray;
        border-radius: 10px;
        opacity: 60%;
        position:absolute;
        width:100%;
        height: 100%;
        z-index: -1;
    }
    .is-main-color {
        color: #e54b4b;
    }
    .button.is-main {
        
        background-color: #e54b4b; 
        border-color: #e54b4b;
        color: whitesmoke;
    }
    .section.is-medium {
        padding-bottom: 0;
    }
</style>