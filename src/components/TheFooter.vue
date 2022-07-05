<template>
    <footer class="py-5">
        <div class="container">
            <div class="row mb-4">
                <div class="col">
                    <!-- Indirizzo -->
                    <h6>Address</h6>
                    <ul class="small-text">
                        <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
                        <li>+1(305)547-9909 (9am - 5pm EST, Monday - Friday)</li>
                        <li>support@maxcoach.com</li>
                    </ul>
                    <div>
                        <a href="#" class="clickable">
                            <i class="fa-brands fa-facebook-square"></i>
                        </a>
                        <a href="#" class="clickable">
                            <i class="fa-brands fa-twitter"></i>
                        </a>
                        <a href="#" class="clickable">
                            <i class="fa-brands fa-instagram"></i>
                        </a>
                        <a href="#" class="clickable">
                            <i class="fa-brands fa-linkedin"></i>
                        </a>
                    </div>
                </div>
                <div class="col row gx-0">
                    <CategoryLinks v-for="category in footerLinks" :key="category.title" :category-data="category"/>
                </div>
            </div>
            <div class="copyright text-center">
                &copy; Maxcoach. All Rights Reserved
            </div>
        </div>
    </footer>
</template>

<script>
    import CategoryLinks from './footer/CategoryLinks';

    export default {
        components: {
            CategoryLinks
        },

        data() {
            return {
                footerLinks: [
                    {
                        title: "Explore",
                        links: [
                            "Start here",
                            "Blog",
                            "About us"
                        ]
                    },
                    {
                        title: "no-title",
                        links: [
                            "Success story",
                            "Courses",
                            "Contact us"
                        ]
                    },
                    {
                        title: "Information",
                        links: [
                            "Membership",
                            "Purchase guide",
                            "Privacy policy",
                            "Terms of service"
                        ]
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    footer {
        background: #171621;
        color: #ABABAB;
        
        h6 {
            color: white;
        }
        ul {
            margin-bottom: 0;

            li {
                padding: 0.3rem 0;
            }
        }
        .copyright {
            font-size: 0.7rem;
        }
    }
</style>
