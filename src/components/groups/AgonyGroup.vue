<template>
    <ItemGroup single>
        <ItemTracker image="shard_of_agony" name="Shard of Agony" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'AgonyGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
