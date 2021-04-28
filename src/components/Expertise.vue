<template>
  <section class="section px-0">
      <div class="columns mx-0">
            <div class="column is-one-third pt-0">
                <figure class="image">
                    <img src="https://shreethemes.in/cristino/layouts/images/skills.jpg">
                </figure>
            </div>
            <div class="column is-two-thirds px-6">
                <heading title="WORK EXPERTISE">
                    Obviously I'm a Web Designer.
                    Experienced with all stages of the development cycle for dynamic web projects.
                </heading>
                <div class="columns p-6">
                    <div class="column is-one-quarter">
                        <button 
                            class="button is-large is-fullwidth mt-3" :class="{active: active==value}"
                            v-for="value,index in Object.keys(expertises)"
                            :key="'button-'+index"
                            @click="active=value"
                        >
                         {{value}}
                        </button>


                    </div>
                    <div class="column is-three-quarters bars">
                        <table>
                        <tr v-for="(skill,index) in expertises[active]" :key="active +'-skill-'+index"><td>
                            <progress-bar :title="skill.name" :value="skill.value"></progress-bar>
                        </td></tr>
                        </table>
                    </div>
                </div>
            </div>
      </div>
  </section>
</template>

<script>
import Heading from './Heading.vue'
import ProgressBar from './ProgressBar.vue';
export default {
  components: { Heading, ProgressBar },
  created(){
      this.active = Object.keys(this.expertises)[0];
  },
  data(){
      return {
          expertises: {
              "UX Design": [
                  {name: 'HTML', value:84},
                  {name: 'CSS', value:75},
                  {name: 'JQuery', value:79},

              ],
              "Language Skill": [
                    {name: 'English', value:84},
                    {name: 'Spanish', value:75},
                    {name: 'German', value:79},
              ],
              "Web Development": [
                    {name: 'Photoshop', value:84},
                    {name: 'Sketch', value:75},
              ]
          },
          active: null
      }
  }
}
</script>

<style scoped>
    section>.columns {
        border-top: 1px solid lightgrey;
    }
    .image {
        overflow: hidden;
        height: 600px;
    }
    img {
        margin-top: -150px;
    }
    .bars {
        vertical-align: middle;
    }
    table {
        width: 100%;
        height: 100%;
    }
    td {
        vertical-align: middle;
    }
    .button.active {
        background-color: orangered;
        color: white;
    }
    .button:focus, .button.is-focused {
        border-color: transparent;
        box-shadow: none;
    }
</style>