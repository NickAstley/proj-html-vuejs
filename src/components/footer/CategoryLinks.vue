<template>
    <div class="col">
        <h6 :class="categoryData.title === `no-title` ? `invisible` : ``">{{categoryData.title}}</h6>
        <ul class="small-text">
            <li v-for="link in categoryData.links" :key="link">
                <a href="#">
                    {{link}}
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: {
            categoryData: Object 
        }
    }
</script>