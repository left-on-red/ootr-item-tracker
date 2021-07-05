<template>
    <ItemGroup single>
        <ItemTracker image="slingshot" name="Fairy Slingshot" :labels="['30', '40', '50']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'SlingshotGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
