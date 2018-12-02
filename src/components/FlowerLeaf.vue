<template>
    <g :mask="maskAttribute" @click="mouseOver">
        <circle cx="290.5" cy="313" :r="options.scoreCircleRadius" :fill="options.scoreCircleColor" />

        <circle cx="290.5" cy="313" :r="230" fill="none" stroke="black" stroke-dasharray="9"/>
    </g>
</template>

<script>
    export default {
        name: "FlowerLeaf",
        props: [
            'options',
            'number'
        ],
        computed: {
            maskAttribute: function () {
                var index = this.options.id - 1;
                return 'url(#mask' + index + ')';
            }
        },
        methods: {
            mouseOver: function () {
                console.log(this.options.id);
            }
        }
    }
</script>

<style scoped>

</style>