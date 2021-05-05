<template>
 <section class="section py-0">
      <div class="columns mx-0">
            <div class="column is-two-thirds px-6">
                <heading title="Clients Say">
                    Obviously I'm a Web Designer.
                    Experienced with all stages of the development cycle for dynamic web projects.
                </heading>
                <div class="container mx-6 px-6">
                    <carousel :data="reviews"></carousel>
                </div>
            </div>
            <div class="column is-one-third pt-0">
                <figure class="image">
                    <img src="https://shreethemes.in/cristino/layouts/images/testi.jpg">
                </figure>
            </div>

      </div>
  </section>
</template>

<script>
import Carousel from './Carousel.vue'
import Heading from './Heading.vue'
export default {
  components: { Heading, Carousel },
    data(){
        return {
            reviews: [
                {
                    rating: 5,
                    quote: "Design Quality",
                    text: "There are many variations of passages of Lorem Ipsum available, by injected humour, or randomised words which don't look even slightly believable.",
                    name: 'Erich Bissonette',
                    organisation: 'Oppo',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/01.jpg'
                },
                                {
                    rating: 5,
                    quote: 'Code Quality',
                    text: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form",
                    name: 'Tina Meyer',
                    organisation: 'Vivo',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/02.jpg'
                },
                                {
                    rating: 5,
                    quote: "Feature Availability",
                    text: "If you are going to use a passage of Lorem Ipsum, you need to be sure there isn't anything embarrassing hidden in the middle of text.",
                    name: 'Sharon Murdock',
                    organisation: 'Apple',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/03.jpg'
                },
                                {
                    rating: 5,
                    quote: 'Customizability',
                    text: "All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.",
                    name: 'Jesse Hunt',
                    organisation: 'Samsung',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/04.jpg'
                },
                                {
                    rating: 5,
                    quote: 'Flexibility',
                    text: "There are many variations of passages of Lorem Ipsum available, by injected humour, or randomised words which don't look even slightly believable.",
                    name: 'Andrea Toy',
                    organisation: 'Nokia',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/05.jpg'
                },
                                                {
                    rating: 5,
                    quote: 'Development',
                    text: "It uses a dictionary of over 200 Latin words, combined with a handful of model sentence structures, to generate Lorem Ipsum which looks reasonable.",
                    name: 'Jay Allums',
                    organisation: 'RedMI',
                    image: 'https://shreethemes.in/cristino/layouts/images/client/06.jpg'
                }
            ]
        }
    }
}
</script>

<style scoped>
    .image {
        overflow: hidden;
        height: 600px;
    }
    img {
        margin-top: -150px;
    }
</style>