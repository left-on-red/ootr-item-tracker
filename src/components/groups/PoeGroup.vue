<template>
    <ItemGroup single>
        <ItemTracker image="poe_soul" name="Big Poes" :labels="['1', '2', '3', '4', '5', '6', '7', '8', '9', '10']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'PoeGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
