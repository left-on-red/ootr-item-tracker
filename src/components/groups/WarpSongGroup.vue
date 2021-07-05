<template>
    <ItemGroup row>
        <ItemTracker image="prelude_of_light" name="Prelude of Light" />
        <ItemTracker image="minuet_of_forest" name="Minuet of Forest" />
        <ItemTracker image="bolero_of_fire" name="Bolero of Fire" />
        <ItemTracker image="serenade_of_water" name="Serenade of Water" />
        <ItemTracker image="nocturne_of_shadow" name="Nocturne of Shadow" />
        <ItemTracker image="requiem_of_spirit" name="Requiem of Spirit" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'WarpSongGroup',
    components: { ItemGroup, ItemTracker }
}
</script>