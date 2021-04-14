<template>
  <section class="section">
    <div class="container">
        <heading title="What do I offer?">
            Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.
        </heading>
        <section class="section">
            <div class="columns is-multiline">
                <div class="column is-one-third" v-for="(offer, index) in offers" :key="index">
                    <offer-card :icon="offer.icon" :title="offer.title" :text="offer.text"></offer-card>
                </div>
            </div>
        </section>
    </div>
  </section>
</template>

<script>
import Heading from './Heading.vue'
import OfferCard from './OfferCard.vue'
export default {
  components: { Heading, OfferCard },
    data(){
        return {
            offers: [
                {
                    icon: 'fas fa-pencil-ruler',
                    title: 'UX / UI Design',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                },
                                {
                    icon: 'fab fa-app-store',
                    title: 'Ios App Designer',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                },
                                {
                    icon: 'fas fa-camera',
                    title: 'Photography',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                },
                                {
                    icon: 'fas fa-brush',
                    title: 'Graphic Designer',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                },                {
                    icon: 'fas fa-user-lock',
                    title: 'Web Security',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                },
                                {
                    icon: 'fas fa-clock',
                    title: '24 / 7',
                    text: 'It is a long established fact that a reader will be distracted by the when looking at its layout.'
                }
            ]
        }
    }
}
</script>

<style scoped>
    section {
        background: #f9fafd;
    }
</style>