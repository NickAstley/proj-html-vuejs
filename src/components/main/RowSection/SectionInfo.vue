<template>
    <div class="col-4">
        <!-- Sottotitolo -->
        <div class="text-uppercase mb-3 grey-text">
            <span>{{sectionData.subtitle.normal}}</span>
            <span class="fw-semibold"> {{sectionData.subtitle.bold}}</span>
        </div>
        <!-- Titolo -->
        <h2 class="display-5 fw-semibold mb-3">
            <span>{{sectionData.title.normal[0]}}</span>
            <span class="text-primary fw-light"> {{sectionData.title.bold}}</span>
            <span v-if="sectionData.title.normal[1]"> {{sectionData.title.normal[1]}}</span>
        </h2>
        <p class="small-text mb-4 grey-text">
            <span>{{sectionData.p[0]}}</span>
            <br>
            <span v-if="sectionData.p[1]">{{sectionData.p[1]}}</span>
        </p>
        <span v-if="sectionData.spanText" class="grey-text">{{sectionData.spanText}} </span>
        <a v-if="sectionData.link" href="#" class="fw-semibold" :class="sectionData.link.color">{{sectionData.link.text}} <i class="fa-solid fa-arrow-right-long"></i></a>
        <button v-if="sectionData.buttonText" class="btn btn-primary fw-bold px-5 py-3">{{sectionData.buttonText}}</button>
    </div>
</template>

<script>
    export default {
        props: {
            sectionData: Object
        }
    }
</script>