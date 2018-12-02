<template>
    <g :id="'leaf' + options.id">
        <flower-leaf-contour :number="options.id - 1" :shadow="false"></flower-leaf-contour>
        <g :mask="maskAttribute">
            <circle cx="290.5" cy="313" :r="options.scoreCircleRadius" :fill="options.scoreCircleColor" />
            <circle cx="290.5" cy="313" :r="options.thresholdScore" fill="none" stroke="black" stroke-dasharray="9"/>
        </g>
    </g>
</template>

<script>
    import FlowerLeafContour from './FlowerLeafContour';
    export default {
        name: "FlowerLeaf",
        components: {
            FlowerLeafContour
        },
        props: [
            'options',
            'number'
        ],
        computed: {
            maskAttribute: function () {
                let index = this.options.id - 1;
                return 'url(#mask' + index + ')';
            }
        },
        methods: {
            mouseOver: function () {
                this.$emit('mouse-over-leaf', this.option.id);
            }
        }
    }
</script>

<style scoped>

</style>