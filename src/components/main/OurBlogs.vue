<template>
    <section class="our-blogs">
        <div class="container">
            <!-- Blocco con titolo -->
            <div class="text-center mb-5">
                <div class="text-uppercase mb-3 grey-text">Read for more joyment</div>
                <h2 class="display-5 fw-semibold mb-3">Latest From <span class="text-primary fw-light">Our Blogs</span></h2>   
            </div>
            <!-- Slider dei corsi -->
            <div class="row row-cols-3 gx-4 mb-3">
                <ItemCard v-for="(post, i) in blogPosts" :key="i" :item-info="post"/>
            </div>
        </div>
    </section>
</template>

<script>
    import ItemCard from './ItemCard'

    export default {
        components: {
            ItemCard
        },
        data() {
            return {
                blogPosts: [
                    {
                        type: "blog",
                        img_src: "img/blog-00.jpeg",
                        category: "artist",
                        title: "Brush Strokes Energize Trees in Paintings",
                        date: "May 15, 2020",
                        viewCount: "688"
                    },
                    {
                        type: "blog",
                        img_src: "img/blog-01.jpg",
                        category: "artist",
                        title: "Pocket-Sized Notebooks Hold Miniature Paintings",
                        date: "May 15, 2020",
                        viewCount: "603"
                    },
                    {
                        type: "blog",
                        img_src: "img/blog-02.jpg",
                        category: "artist",
                        title: "Connection Between Self-Portraits and Identity",
                        date: "May 15, 2020",
                        viewCount: "397"
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    .our-blogs {
        margin-top: 5rem;
        background: #F8F8F8;
    }
</style>