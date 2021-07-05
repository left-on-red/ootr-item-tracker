<template>
    <div @click="forward" @contextmenu.prevent="backward" class="tracker" :style="`width: ${unit_size}px; height: ${unit_size}px;`">
        <img :src="image_source" :key="image_source" :style="`${item_index < 0 ? 'filter: brightness(25%);' : 'filter: brightness(75%);'} width: ${unit_size}px; height: ${unit_size}px;`" draggable="false" />
        <p :key="label_source" class="label" :style="`color: ${label_color_source};`">{{label_source}}</p>
    </div>
</template>

<script>
export default {
    name: 'ItemTracker',
    
    props: {
        image: {
            required: false,
            type: String
        },

        images: {
            required: false,
            type: Array
        },

        name: {
            required: false,
            type: String
        },

        names: {
            required: false,
            type: Array
        },

        counter: {
            required: false,
            type: Boolean
        },

        max: {
            required: false,
            type: String
        },

        labels: {
            required: false,
            type: Array
        },

        label_color: {
            required: false,
            type: String
        },

        label_max_color: {
            required: false,
            type: String
        },

        no_max_color: {
            required: false,
            type: Boolean
        },

        unit_size: {
            type: String,
            default: '35'
        }
    },

    //props: [ 'image', 'images', 'name', 'names', 'counter', 'max', 'labels', 'label_color', 'label_max_color', 'no_max_color' ],
    
    data: () => ({
        item_index: -1
    }),

    computed: {
        image_array() {
            if (this.images && this.images instanceof Array) { return this.images }
            else if (this.image && typeof this.image == 'string') { return [this.image] }
            return [];
        },

        name_array() {
            if (this.names && this.names instanceof Array) { return this.names }
            else if (this.name && typeof this.name == 'string') { return [this.name] }
            return [];
        },

        label_array() {
            if (this.labels && this.labels instanceof Array) { return this.labels }
            return [];
        },

        image_source() {
            let usable_index = this.item_index;
            if (this.counter) { usable_index = 0 }
            else if (usable_index > this.image_array.length - 1) { usable_index = this.image_array.length - 1 }

            if (usable_index == -1) { usable_index = 0 }
            return require(`./../assets/items/${this.image_array[usable_index]}.png`)
        },

        name_source() {
            let usable_index = this.item_index < 0 ? 0 : this.item_index > this.name_array.length - 1 ? this.item_index : this.name_array.length - 1;
            return this.name_array[usable_index];
        },

        label_color_source() {
            let color = this.label_color ? typeof this.label_color == 'string' ? this.label_color : '#F1F1F1' : '#F1F1F1';
            let max_color = this.no_max_color ? color : this.label_max_color ? typeof this.label_max_color == 'string' ? this.label_max_color : '#20FF20' : '#20FF20';
            
            if (this.counter && this.item_index + 1 == parseInt(this.max)) { return max_color }
            else if (this.item_index == this.label_array.length - 1) { return max_color }
            else { return color }

        },

        label_source() {
            if (this.label_array.length > 0) { return this.item_index >= 0 ? this.label_array[this.item_index] != undefined ? this.label_array[this.item_index] : this.label_array[this.label_array.length - 1] : '' }
            else if (this.counter && this.item_index >= 0) { return `${this.item_index + 1}` }
            else { return '' }
        }
    },

    methods: {
        forward() {
            if (this.counter && this.item_index < parseInt(this.max) - 1) { this.item_index += 1 }
            else {
                let total = Math.max(this.image_array.length, Math.max(this.name_array.length, this.label_array.length));
                if (this.item_index < total - 1) { this.item_index += 1 }
            }
        },

        backward() {
            if (this.item_index != -1) { this.item_index -= 1 }
        }
    }
}
</script>

<style scoped>
    div {
        position: relative;
        margin: 0;
        padding: 0;
        background-color: rgba(0, 0, 255, 0.5);
        display: inline-block;
    }

    div p.label {
        position: absolute;
        right: 0;
        bottom: 0;
        margin: 0;
        padding: 2px;
        font-size: 20px;
        cursor: default;
        user-select: none;
        font-family: 'square';
    }
</style>
