<template>
    <ItemGroup single>
        <ItemTracker :images="['hookshot', 'longshot']" :names="['Hookshot', 'Longshot']" :labels="['H', 'L']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'HookshotGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
