<template>
    <g :id="'leaf' + options.id" @mouseover="mouseOver" @mouseout="mouseOut">
        <flower-leaf-contour :number="options.id - 1" :hover="this.hover"></flower-leaf-contour>
        <g :clip-path="clipAttribute">
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
        data: function() {
          return {
              'hover': false
          };
        },
        props: [
            'options',
            'number'
        ],
        computed: {
            clipAttribute: function () {
                let index = this.options.id - 1;
                return 'url(#clip_path' + index + ')';
            }
        },
        methods: {
            mouseOver: function () {
                this.hover = true;
                this.$emit('mouse-over-leaf', this.option.id);
            },
            mouseOut: function () {
                this.hover = false;
                this.$emit('mouse-out-leaf', this.option.id);
            }
        }
    }
</script>

<style scoped>

</style>