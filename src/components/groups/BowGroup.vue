<template>
    <ItemGroup row>
        <ItemTracker image="bow" name="Fairy Bow" :labels="['30', '40', '50']" />
        <ItemTracker image="fire_arrow" name="Fire Arrows" />
        <ItemTracker image="ice_arrow" name="Ice Arrows" />
        <ItemTracker image="light_arrow" name="Light Arrows" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'BowGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
