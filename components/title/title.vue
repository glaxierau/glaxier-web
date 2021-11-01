<template>
    <div class="flex flex-col justify-center items-center">
        <curvy-line :color="lineColor" :width="lineWidth"/>
        <h2>{{title}}</h2>
    </div>
</template>

<script>
import CurvyLine from '../lines/curvyline.vue'
export default {
    name: 'Title',
    components: {
        CurvyLine
    },
    props: {
        title: {
            type: String,
            default:''
        }, 
        lineColor: {
            type: String,
            default: '#fff'
        },
        lineWidth: {
            type: Number,
            default: 0
        }},
}
</script>

<style scoped>

</style>