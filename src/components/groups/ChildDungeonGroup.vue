<template>
    <ItemGroup row unit_size="40">
        <DungeonTreasureTracker label="deku" starting_index="0" />
        <DungeonTreasureTracker label="DC" starting_index="1" />
        <DungeonTreasureTracker label="jabu" starting_index="2" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import DungeonTreasureTracker from './../DungeonTreasureTracker.vue';

export default {
    name: 'ChildDungeonGroup',
    components: { ItemGroup, DungeonTreasureTracker }
}
</script>
