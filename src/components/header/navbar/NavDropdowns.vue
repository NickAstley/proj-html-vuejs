<template>
    <ul class="nav-dropdowns">
        <!-- Stampo con un ciclo i vari dropdown della navbar -->
        <li class="nav-item dropdown mx-3" v-for="dropdown in dropdownsList" :key="dropdown">
            <a class="nav-link" href="#" :id="dropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                {{ dropdown }}
                <i class="fa-solid fa-angle-down"></i>
            </a>
            <!-- Aggiungo ad ogni dropdown due link casuali, giusto per controllarne il funzionamento -->
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                <li>
                    <a class="dropdown-item" href="#">Azione di esempio</a>
                </li>
                <li>
                    <a class="dropdown-item" href="#">Azione di esempio 2</a>
                </li>
            </ul>
        </li>
    </ul>
</template>

<script>
    export default {
        props: {
            dropdownsList: Array
        }
    }
</script>

<style lang="scss">
    .nav-dropdowns {

        .nav-item.dropdown {
            display: inline-block;

            i {
                font-size: 0.7rem;
            }
        }
    }
</style>