<template>
    <div @click="forward" @contextmenu.prevent="backward" class="tracker">
        <img :src="image_source" :key="image_source" :style="!obtained ? 'filter: brightness(25%);' : 'filter: brightness(75%);'" draggable="false" />
        <p class="label">{{label}}</p>
    </div>
</template>

<script>

let treasures = [
    'kokiri_emerald',
    'goron_ruby',
    'zora_sapphire',
    'light_medallion',
    'forest_medallion',
    'fire_medallion',
    'water_medallion',
    'shadow_medallion',
    'spirit_medallion'
]

export default {
    name: 'DungeonTreasureTracker.vue',

    props: {
        label: {
            required: true,
            type: String
        },

        starting_index: {
            required: true,
            type: String
        }
    },

    data: () => ({
        obtained: false,
        treasure_index: 0
    }),

    mounted() { this.treasure_index = parseInt(this.starting_index) },

    computed: {
        image_source() {
            let image_name = treasures[this.treasure_index];
            return require(`./../assets/items/${image_name}.png`)
        }
    },

    methods: {
        forward() {
            if (!this.obtained) { this.obtained = true }
        },

        backward() {
            if (this.obtained) { this.obtained = false }
            else {
                if (this.treasure_index + 1 == treasures.length) { this.treasure_index = 0 }
                else { this.treasure_index += 1 }
            }
        }
    }
}

</script>

<style scoped>
    div {
        position: relative;
        height: 40px;
        width: 40px;
        margin: 0;
        padding: 0;
        background-color: rgba(0, 0, 255, 0.5);
        display: inline-block;
    }

    div img {
        width: 40px;
        height: 40px;
    }

    div p.label {
        position: absolute;
        left: 0;
        bottom: 0;
        margin: 0;
        display: inline-block;
        font-size: 10px;
        font-weight: 10;
        cursor: default;
        user-select: none;
        font-family: 'square';
        color: #FFF;
        width: 100%;
        text-align: center;
        text-transform: uppercase;
    }
</style>