<template>
    <ItemGroup row unit_size="40">
        <DungeonTreasureTracker label="free" starting_index="3" />
        <DungeonTreasureTracker label="forest" starting_index="4" />
        <DungeonTreasureTracker label="fire" starting_index="5" />
        <DungeonTreasureTracker label="water" starting_index="6" />
        <DungeonTreasureTracker label="shadow" starting_index="7" />
        <DungeonTreasureTracker label="spirit" starting_index="8" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import DungeonTreasureTracker from './../DungeonTreasureTracker.vue';

export default {
    name: 'AdultDungeonGroup',
    components: { ItemGroup, DungeonTreasureTracker }
}
</script>
