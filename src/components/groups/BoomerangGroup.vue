<template>
    <ItemGroup single>
        <ItemTracker image="boomerang" name="Boomerang" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'BoomerangGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
