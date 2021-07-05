<template>
    <ItemGroup row>
        <ItemTracker image="kokiri_boots" name="Kokiri Boots" />
        <ItemTracker image="iron_boots" name="Iron Boots" />
        <ItemTracker image="hover_boots" name="Hover Boots" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'BootsGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
