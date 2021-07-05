<template>
    <ItemGroup single>
        <ItemTracker image="deku_nut" name="Deku Nuts" :labels="['20', '30', '40']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'NutGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
