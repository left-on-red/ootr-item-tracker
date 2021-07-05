<template>
    <ItemGroup row>
        <ItemTracker image="zeldas_lullaby" name="Zelda's Lullaby" />
        <ItemTracker image="eponas_song" name="Epona's Song" />
        <ItemTracker image="sarias_song" name="Saria's Song" />
        <ItemTracker image="suns_song" name="Suns Song" />
        <ItemTracker image="song_of_time" name="Song of Time" />
        <ItemTracker image="song_of_storms" name="Song of Storms" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'UtilitySongGroup',
    components: { ItemGroup, ItemTracker }
}
</script>