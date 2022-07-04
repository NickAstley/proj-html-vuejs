<template>
    <div class="col-4">
        <div class="text-uppercase mb-3">{{sectionData.subtitle.normal}} <span class="fw-semibold">{{sectionData.subtitle.bold}}</span></div>
        <h2 class="display-5 fw-semibold mb-3">{{sectionData.title.normal[0]}} <span class="text-primary fw-light">{{sectionData.title.bold}}</span> {{sectionData.title.normal[1]}}</h2>
        <p class="small-text mb-4">{{sectionData.p[0]}}<br>{{sectionData.p[1]}}</p>
        <span>{{sectionData.span}} </span>
        <a href="#" class="fw-semibold" :class="sectionData.link.color">{{sectionData.link.text}} <i class="fa-solid fa-arrow-right-long"></i></a>
    </div>
</template>

<script>
    export default {
        props: {
            sectionData: Object
        }
    }
</script>