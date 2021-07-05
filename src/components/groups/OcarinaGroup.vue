<template>
    <ItemGroup single>
        <ItemTracker :images="['fairy_ocarina', 'ocarina_of_time']" :names="['Fairy Ocarina', 'Ocarina of Time']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'OcarinaGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
