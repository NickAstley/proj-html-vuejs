<template>
    <nav class="row justify-content-around align-items-center">
        <!-- Importo il componente che gestisce i dropdown -->
        <NavDropdowns class="col-auto" :dropdowns-list="dropdownsList"/>
        <!-- Logo -->
        <div class="col-auto">
            <img class="logo py-4" src="../../../public/img/dark-logo.png" alt="Logo MaxCoach">
        </div>
        <!-- Menu di ricerca, accesso al carrello e al profilo -->
        <div class="nav-menu col-auto">
            <div class="row align-items-center">
                <!-- Icona del carello con numero di elementi in absolute -->
                <div class="col-auto">
                    <a href="#" class="cart-icon-container clickable-icon">
                        <i class="fa-solid fa-cart-shopping"></i>
                        <div class="item-counter">
                            0
                        </div>
                    </a>
                </div>
                <!-- Icona del profilo -->
                <div class="col-auto">
                    <a class="clickable-icon" href="#">
                        <i class="fa-regular fa-circle-user"></i>
                    </a>
                </div>
                <!-- Barra di ricerca -->
                <div class="col">
                    <div class="search-input">
                        <input class="form-control" type="text" placeholder="Search...">
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
        .logo {
            width: 158px;
        }
        .nav-menu {
            .cart-icon-container {
                position: relative;

                .item-counter {
                    position: absolute;
                    top: -50%;
                    right: -50%;
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
                    font-size: 0.9rem;
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