<template>
    <ItemGroup>
        <ItemTracker image="bottle" name="Bottle" :labels="['1', '2', '3', '4']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'BottleGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
