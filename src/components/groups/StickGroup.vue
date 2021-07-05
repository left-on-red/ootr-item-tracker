<template>
    <ItemGroup single>
        <ItemTracker image="deku_stick" name="Deku Sticks" :labels="['10', '20', '30']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'StickGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
