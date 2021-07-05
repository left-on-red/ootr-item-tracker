<template>
    <div class="container" :style="style_source">
        <slot></slot>
    </div>
</template>

<script>

export default {
    name: 'Container',
    props: {
        width: {
            type: String,
            required: false
        },

        height: {
            type: String,
            required: false
        },

        unit_size: {
            type: String,
            default: '35'
        }
    },

    computed: {
        style_source() {
            let style = '';
            if (this.width) { style += `width: ${this.width * parseInt(this.unit_size)}px;` }
            if (this.height) { style += `height: ${this.height * parseInt(this.unit_size)}px;` }
            return style;
        }
    }
}
</script>

<style scoped>
    div.container {
        margin: 0;
        padding: 0;
        display: inline-block;
        float: left;
    }
</style>

