<template>
    <svg width="400" height="520" style="fill:none">
        <flower-leaf></flower-leaf>
        <defs id="defs1196">
            <filter id="filter0_d"
                    x="98.640602"
                    y="0.23205601"
                    width="218.32401"
                    height="331.599"
                    filterUnits="userSpaceOnUse"
                    style="color-interpolation-filters:sRGB">

                <feFlood
                        flood-opacity="0"
                        result="BackgroundImageFix"
                        id="feFlood1181" />

                <feColorMatrix
                        in="SourceAlpha"
                        type="matrix"
                        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                        id="feColorMatrix1183" />
                <feOffset
                        id="feOffset1185" />
                <feGaussianBlur
                        stdDeviation="15"
                        id="feGaussianBlur1187" />
                <feColorMatrix
                        type="matrix"
                        values="0 0 0 0 0.631271 0 0 0 0 0.631271 0 0 0 0 0.631271 0 0 0 0.589278 0"
                        id="feColorMatrix1189" />
                <feBlend
                        mode="normal"
                        in2="BackgroundImageFix"
                        result="effect1_dropShadow"
                        id="feBlend1191" />
                <feBlend
                        mode="normal"
                        in="SourceGraphic"
                        in2="effect1_dropShadow"
                        result="shape"
                        id="feBlend1193" />
            </filter>
        </defs>
    </svg>
</template>

<script>
    import FlowerLeaf from './FlowerLeaf'
    export default {
        name: "Flower",
        components: {
            FlowerLeaf
        },
        data() {
            return {

            }
        }
    }
</script>

<style scoped>

</style>