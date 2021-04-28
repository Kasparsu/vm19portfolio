<template>
  <section class="section">
      <div class="container is-max-desktop">
                  <heading title="My Portfolio">
                    Obviously I'm a Web Designer. Experienced with all stages of the development cycle for dynamic web projects.
                </heading>
                <div class="filter py-3">
                    <button class="button mr-1 is-capitalized" v-for="tag in tags" :key="tag" @click="filter=tag">{{tag}}</button>
                </div>
                <div class="columns is-multiline">
                    <div class="column is-one-third" v-for="(item,index) in filteredItems" :key="index">
                        <portfolio-item :data="item" @gallery="openGallery"></portfolio-item>
                    </div>
                </div>
      </div>
      <gallery :images="galleryImages" @close="galleryOpen=false" v-if="galleryOpen"></gallery>
  </section>
</template>

<script>
import Gallery from './Gallery.vue'
import Heading from './Heading.vue'
import PortfolioItem from './PortfolioItem.vue'
export default {
  components: { Heading, PortfolioItem, Gallery },
    data() {
        return {
            items: [
                {title: 'Working Keyboard', tags: ['branding', 'design'], images: ['https://picsum.photos/seed/portfolio1/400/300','https://picsum.photos/seed/portfolio11/200/300']},
                {title: 'The Micro Headphones', tags: ['development', 'design'], images: ['https://picsum.photos/seed/portfolio2/400/300','https://picsum.photos/seed/portfolio22/200/300']},
                {title: 'The Wooden Desk', tags: ['branding', 'photography'], images: ['https://picsum.photos/seed/portfolio3/400/300','https://picsum.photos/seed/portfolio33/200/300']},
                {title: 'Camera', tags: ['illustrations', 'photography'], images: ['https://picsum.photos/seed/portfolio4/400/300','https://picsum.photos/seed/portfolio44/200/300']},
                {title: 'Branded Laptop', tags: ['development', 'branding'], images: ['https://picsum.photos/seed/portfolio5/400/300','https://picsum.photos/seed/portfolio55/200/300']},
                {title: 'The Coffee Cup', tags: ['illustrations', 'branding'], images: ['https://picsum.photos/seed/portfolio6/400/300','https://picsum.photos/seed/portfolio66/200/300']},
            ],
            filter: 'all',
            galleryOpen: false,
            galleryImages: []
        }
    },
    methods: {
        openGallery(images){
            this.galleryOpen = true;
            this.galleryImages = images;
        }
    },
    computed: {
        tags() {
            return ['all', ...this.items.reduce((tags, item)=>{
                tags.push(...item.tags);
                return tags.filter((v, i, a) => a.indexOf(v) === i);
            }, [])];
        },
        filteredItems(){
            return this.items.filter(item => {
                if(this.filter === 'all'){
                    return true;
                }
                return item.tags.includes(this.filter);
            })
        }
    }
}
</script>

<style scoped>
    section {
        background-color: #f9fafd;
    }
    .filter {
        text-align: center;
    }
</style>