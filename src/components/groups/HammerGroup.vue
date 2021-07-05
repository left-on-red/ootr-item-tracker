<template>
    <ItemGroup single>
        <ItemTracker image="hammer" name="Megaton Hammer" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'HammerGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
