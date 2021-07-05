<template>
    <ItemGroup>
        <ItemTracker image="dins_fire" name="Din's Fire" />
        <ItemTracker image="farores_wind" name="Farore's Wind" />
        <ItemTracker image="nayrus_love" name="Nayru's Love" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'SpellsGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
