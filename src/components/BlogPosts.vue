<template>
  <section class="section">
      <div class="container">
          <heading title="LATEST NEWS & BLOG">Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.</heading>
          <div class="columns mt-3">
              <div class="column is-one-third" v-for="(post, index) in posts" :key="index">
                  <blog-post-card :data="post"></blog-post-card>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import BlogPostCard from './BlogPostCard.vue'
import Heading from './Heading.vue'
export default {
  components: { Heading, BlogPostCard },
    data(){
        return {
            posts: [
                {
                    title: 'Our Home Entertainment has Evolved Significantly',
                    image: 'https://shreethemes.in/cristino/layouts/images/blog/01.jpg',
                    tag: 'Branding',
                    created: '10th April, 2020',
                    user:'kaspar'
                },
                                {
                    title: 'These Are The Voyages of The Starship Enterprise',
                    image: 'https://shreethemes.in/cristino/layouts/images/blog/02.jpg',
                    tag: 'Branding',
                    created: '10th April, 2020',
                    user:'kaspar'
                },
                {
                    title: 'Three Reasons Visibility Matters in Supply Chain',
                    image: 'https://shreethemes.in/cristino/layouts/images/blog/03.jpg',
                    tag: 'Branding',
                    created: '10th April, 2020',
                    user:'kaspar'
                }
            ]
        }
    }
}
</script>

<style scoped>
    section {
        background-color: #f9fafd;
    }
</style>