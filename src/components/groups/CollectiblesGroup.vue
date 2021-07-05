<template>
    <ItemGroup row>
        <ItemTracker image="heart_container" name="Heart Container" counter max="8" />
        <ItemTracker image="piece_of_heart" name="Piece of Heart" counter max="36" />
        <ItemTracker image="skull_token" name="Gold Skulltulas" counter max="100" />
        <ItemTracker image="heart_container" name="Double Defense" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'CollectiblesGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
