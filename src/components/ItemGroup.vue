<template>
    <div class="group" :style="row ? `height: ${unit_size}px;` : `width: ${unit_size}px;`">
        <div class="inner" :style="`${single ? `height: ${parseInt(unit_size) - offset}px; width: ${parseInt(unit_size) - offset}px;` : row ? `height: ${parseInt(unit_size) - offset}px; width: ${(tracker_count * parseInt(unit_size)) - offset}px;` : `width: ${parseInt(unit_size) - offset}px; height: ${(tracker_count * parseInt(unit_size)) - offset}px;`} margin: ${offset / 2}px;`"></div>
        <div class="trackers" ref="trackers">
            <slot></slot>
        </div>
    </div>
</template>

<script>

export default {
    name: 'ItemGroup',
    data: () => ({
        tracker_count: 0,
        offset: 6
    }),

    props: {
        row: {
            required: false,
            type: Boolean
        },

        single: {
            required: false,
            type: Boolean
        },

        unit_size: {
            type: String,
            default: '35'
        }
    },

    mounted() {
        this.tracker_count = this.$refs.trackers.children.length;
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    div {
        margin: 0;
        padding: 0;
        display: inline-block;
        float: left;
    }

    div.inner {
        background-color: red;
        position: absolute;
        border-radius: 4px;
    }
</style>
