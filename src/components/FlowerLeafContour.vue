<template>
    <g>
        <g :filter="hover ? 'url(#shadow)' : ''" >
            <path fill-rule="evenodd" clip-rule="evenodd" :d="options[number].path" :fill="hover ? '#FFFFFF' : '#EFEFEF'" />
        </g>
        <clipPath :id="'clip_path' + number" mask-type="alpha" maskUnits="userSpaceOnUse" :x="options[number].mask.x" :y="options[number].mask.y" :width="options[number].mask.w" :height="options[number].mask.h">
            <path fill-rule="evenodd" clip-rule="evenodd" :d="options[number].path" fill="white"/>
        </clipPath>
        <defs>
            <filter id="shadow" width="120%" height="120%" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                <feGaussianBlur in="SourceAlpha" stdDeviation="5"/>
                <feComponentTransfer>
                    <feFuncA type="linear" slope="0.15"/>
                </feComponentTransfer>
                <feMerge>
                    <feMergeNode />
                    <feMergeNode in="SourceGraphic" />
                </feMerge>
            </filter>
        </defs>
    </g>
</template>

<script>
    export default {
        name: "FlowerLeafContour",
        data: function() {
            return {
                options: [
                    {
                        'path': "M292.567 46.5211V293.768C292.567 303.099 297.006 304.54 302.491 296.995L447.677 96.9593C453.156 89.4136 451.463 78.8608 443.57 73.9054C423.353 61.2071 401.723 51.1105 379.199 43.7843C356.68 36.4582 333.25 31.9026 309.432 30.2808C300.134 29.6502 292.567 37.1903 292.567 46.5211Z",
                        'mask': {
                            'x': 292,
                            'y': 30,
                            'w': 159,
                            'h': 272,
                        }
                    },
                    {
                        "path": "M452.211 100.259L307.042 300.295C301.557 307.84 304.302 311.624 313.168 308.741L548.074 232.327C556.94 229.443 561.772 219.921 558.295 211.266C549.396 189.096 537.819 168.199 523.896 149.019C509.973 129.84 493.699 112.36 475.388 97.0437C468.238 91.0578 457.696 92.7134 452.211 100.259Z",
                        "mask": {
                            "x": 304,
                            "y": 93,
                            "w": 256,
                            "h": 217
                        }
                    }, {

                        "path": "M549.817 237.671L314.911 314.085C306.045 316.963 306.045 321.637 314.911 324.52L549.817 400.923C558.683 403.806 568.19 398.936 570.457 389.886C576.273 366.708 579.187 342.996 579.187 319.294C579.187 295.593 576.273 271.88 570.457 248.708C568.184 239.658 558.683 234.793 549.817 237.671Z",
                        "mask": {
                            "x": 308,
                            "y": 236,
                            "w": 272,
                            "h": 166
                        }
                    }, {
                        "path": "M548.085 406.267L313.173 329.869C304.308 326.992 301.568 330.77 307.047 338.316L452.234 538.34C457.718 545.886 468.266 547.536 475.416 541.55C493.715 526.228 509.99 508.76 523.907 489.58C537.835 470.395 549.413 449.498 558.306 427.333C561.783 418.678 556.951 409.145 548.085 406.267Z",
                        "mask": {
                            "x": 304,
                            "y": 328,
                            "w": 256,
                            "h": 218
                        }
                    }, {
                        "path": "M447.694 541.646L302.496 341.616C297.017 334.07 292.573 335.512 292.573 344.843L292.59 592.107C292.59 601.437 300.156 608.977 309.455 608.341C333.262 606.714 356.692 602.153 379.222 594.821C401.746 587.489 423.375 577.398 443.588 564.7C451.486 559.744 453.168 549.192 447.694 541.646Z",
                        "mask": {
                            "x": 292,
                            "y": 336,
                            "w": 159,
                            "h": 273
                        }
                    }, {
                        "path": "M286.987 592.107L286.97 344.843C286.97 335.512 282.531 334.07 277.052 341.616L131.883 541.668C126.398 549.208 128.091 559.761 135.984 564.717C156.201 577.415 177.837 587.512 200.361 594.838C222.896 602.164 246.326 606.719 270.122 608.341C279.421 608.977 286.987 601.437 286.987 592.107Z",
                        "mask": {
                            "x": 128,
                            "y": 336,
                            "w": 159,
                            "h": 273
                        }
                    }, {
                        "path": "M127.332 538.368L272.507 338.322C277.986 330.776 275.236 326.998 266.37 329.881L31.4693 406.301C22.6036 409.184 17.777 418.712 21.2535 427.367C30.1529 449.531 41.73 470.429 55.6529 489.608C69.5815 508.794 85.8558 526.262 104.161 541.584C111.316 547.564 121.858 545.914 127.332 538.368Z",
                        "mask": {
                            "x": 20,
                            "y": 328,
                            "w": 256,
                            "h": 218
                        }
                    }, {
                        "path": "M29.7422 400.946L264.643 324.525C273.508 321.637 273.508 316.963 264.643 314.085L29.7253 237.699C20.8596 234.816 11.3527 239.692 9.08562 248.736C3.27456 271.914 0.360594 295.626 0.366219 319.328C0.366219 343.029 3.28019 366.742 9.10249 389.914C11.3695 398.964 20.8765 403.835 29.7422 400.946Z",
                        "mask": {
                            "x": 0,
                            "y": 236,
                            "w": 272,
                            "h": 166
                        }
                    }, {
                        "path": "M31.4573 232.36L266.369 308.736C275.235 311.619 277.98 307.835 272.501 300.289L127.298 100.282C121.824 92.736 111.276 91.0804 104.126 97.0607C85.8213 112.389 69.547 129.868 55.6241 149.047C41.7012 168.227 30.1297 189.13 21.2359 211.3C17.765 219.955 22.5916 229.477 31.4573 232.36Z",
                        "mask": {
                            "x": 20,
                            "y": 93,
                            "w": 256,
                            "h": 217
                        }
                    }, {
                        "path": "M131.838 96.9762L277.047 296.995C282.52 304.54 286.964 303.099 286.964 293.768L286.931 46.5042C286.931 37.1734 279.37 29.6333 270.066 30.2696C246.265 31.897 222.835 36.4638 200.305 43.7956C177.781 51.1217 156.151 61.224 135.944 73.9223C128.046 78.8833 126.359 89.4305 131.838 96.9762Z",
                        "mask": {
                            "x": 128,
                            "y": 30,
                            "w": 159,
                            "h": 272
                        }
                    }

                ]
            };
        },
        props: {
            number: Number,
            hover: Boolean
        }
    }
</script>

<style scoped>
    path {
        transition: all 0.4s;
    }
</style>

