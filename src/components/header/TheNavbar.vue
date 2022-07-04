<template>
    <nav class="row justify-content-evenly align-items-center">
        <!-- Importo il componente che gestisce i dropdown -->
        <NavDropdowns class="col-4 text-end mb-0" :dropdowns-list="dropdownsList"/>
        <!-- Logo -->
        <div class="logo-container col-2 text-center">
            <a href="#" class="clickable">
                <img class="logo" src="../../../public/img/dark-logo.png" alt="Logo MaxCoach">
            </a>
        </div>
        <!-- Menu di ricerca, accesso al carrello e al profilo -->
        <div class="nav-menu col-4">
            <div class="row justify-content-center align-items-center gx-0">
                <div class="col-auto">
                    <!-- Icona del carello con numero di elementi in absolute -->
                    <a href="#" class="cart-icon-container clickable">
                        <i class="fa-solid fa-cart-shopping"></i>
                        <div class="item-counter">
                            0
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
                        <input class="form-control small-text" type="text" placeholder="Search...">
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
        .logo-container {
            .clickable {
                padding: 1.5rem;

                .logo {
                    width: 158px;
                }
            }
        }
        .nav-menu {
            .cart-icon-container {
                position: relative;

                .item-counter {
                    position: absolute;
                    top: 6px;
                    right: 6px;
                    background: $primary;
                    width: 1rem;
                    height: 1rem;
                    border-radius: 50%;
                    text-align: center;
                    color: white;
                    font-size: 0.7rem;
                }
            }
            .search-input {
                position: relative;

                input {
                    background: #F5F5F5;
                    border: none;
                    padding: 0.8rem;
                    font-weight: 300;
                }

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