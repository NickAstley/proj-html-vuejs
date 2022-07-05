<template>
    <nav class="row justify-content-evenly align-items-center">
        <!-- Componente che gestisce i dropdown -->
        <NavDropdowns class="col-4 text-end mb-0" :dropdowns-list="dropdownsList"/>
        <!-- Logo -->
        <div class="logo-container col-2 text-center">
            <a href="#" class="clickable">
                <img class="logo" src="img/logo.png" alt="Logo MaxCoach">
            </a>
        </div>
        <!-- Menu di ricerca, accesso al carrello e al profilo -->
        <div class="nav-menu col-4">
            <div class="row justify-content-center align-items-center gx-0">
                <div class="col-auto">
                    <!-- Icona del carello con numero di elementi in absolute -->
                    <a href="#" class="clickable">
                        <div class="position-relative">
                            <i class="fa-solid fa-cart-shopping"></i>
                            <span class="position-absolute top-0 start-100 translate-middle badge rounded-circle bg-primary">0</span>
                        </div>
                    </a>
                    <!-- Icona del profilo -->
                    <a class="clickable" href="#">
                        <i class="fa-regular fa-circle-user"></i>
                    </a>
                </div>
                <!-- Barra di ricerca -->
                <div class="col-6">
                    <div class="search-input">
                        <input class="form-control my-input small-text" type="text" placeholder="Search...">
                        <span class="input-search-icon">
                                <i class="fa fa-search input-search-icon"></i>
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
    import NavDropdowns from './navbar/NavDropdowns';

    export default {
        components: {
            NavDropdowns
        },

        data() {
            return {
                dropdownsList: [
                    "Home",
                    "Pages",
                    "Courses",
                    "Features",
                    "Blog",
                    "Shop"
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../../assets/scss/variables';

    nav {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 99;
        background: white;
        box-shadow: 0px 1px 10px #999;

        .logo-container {

            .clickable {
                padding: 1.5rem;

                .logo {
                    width: 158px;
                }
            }
        }
        .nav-menu {
            
            .search-input {
                position: relative;

                .input-search-icon {
                    position: absolute;
                    top: 0;
                    right: 0.5rem;
                    bottom: 0;
                    color: $primary;
                    display: flex;
                    align-items: center;
                }
            }
        }
    }
    .ms-n5 {
        margin-left: -40px;
    } 
</style>