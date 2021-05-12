<template>
  <section class="section">
      <div class="container">
          <heading title="Contact">Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.</heading>
            <div class="columns">
                <div class="is-one-third">
                    <contact-card 
                    data="+152 534-468-854"
                    data-link="tel:+152 534-468-854"
                    icon="fas fa-phone"
                    title="phone"
                    text="Promising development turmoil inclusive education transformative community"
                    ></contact-card>
                </div>
                <div class="is-one-third">
                    <contact-card 
                    data="contact@example.com"
                    data-link="mailto:contact@example.com"
                    icon="far fa-envelope"
                    title="email"
                    text="Promising development turmoil inclusive education transformative community"
                    ></contact-card>
                </div>
                <div class="is-one-third">
                    <contact-card 
                    data-link="https://www.google.com/maps/place/54+Northwest+Fwy+%23558,+Houston,+TX+77040,+USA/@29.8724285,-95.5545326,20.5z/data=!4m8!1m2!2m1!1sC%2F54+Northwest+Freeway,+Suite+558,+Houston,+USA+485!3m4!1s0x8640cfe4516785ed:0x774974592a609121!8m2!3d29.8724486!4d-95.5543544"
                    data="C/54 Northwest Freeway, Suite 558, Houston, USA 485"
                    icon="fas fa-map-marker-alt"
                    title="location"
                    ></contact-card>
                </div>
            </div>
            <form>
                <div class="columns is-multiline">
                    <div class="column is-half">
                
                        <div class="field">
                            <div class="control">
                                <input class="input" type="text" placeholder="First name:" required>
                            </div>
                        </div>
                        <div class="field">
                            <div class="control">
                                <input class="input" type="email" placeholder="Email:" required>
                            </div>
                        </div>
                        <div class="field">
                            <div class="control">
                                <input class="input" type="text" placeholder="Title:" required>
                            </div>
                        </div>
                    </div>
                    <div class="column is-half">
                        <div class="field">
                            <div class="control">
                                <textarea class="textarea" placeholder="Your message:" required></textarea>
                            </div>
                        </div>
                    </div>
                    <div class="column is-full has-text-right">
                        <input class="button" type="submit" value="Submit">
                    </div>
                </div>
            </form>
      </div>
  </section>
</template>

<script>
import ContactCard from './ContactCard.vue'
import Heading from './Heading.vue'
export default {
  components: { Heading, ContactCard },

}
</script>

<style>

</style>