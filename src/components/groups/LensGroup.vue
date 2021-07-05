<template>
    <ItemGroup single>
        <ItemTracker image="lens_of_truth" name="Lens of Truth" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'LensGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
