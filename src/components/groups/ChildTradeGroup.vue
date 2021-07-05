<template>
    <ItemGroup single>
        <ItemTracker
            :images="[
                'weird_egg',
                'cucco',
                'zeldas_letter',
                'keaton_mask',
                'skull_mask',
                'spooky_mask',
                'bunny_hood',
                'mask_of_truth'
            ]"
            
            :names="[
                'Weird Egg',
                'Cucco',
                'Zelda\'s Letter',
                'Keaton Mask',
                'Skull Mask',
                'Spooky Mask',
                'Bunny Hood',
                'Mask of Truth'
            ]" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'ChildTradeGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
