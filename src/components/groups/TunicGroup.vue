<template>
    <ItemGroup row>
        <ItemTracker image="kokiri_tunic" name="Kokiri Tunic" />
        <ItemTracker image="goron_tunic" name="Goron Tunic" />
        <ItemTracker image="zora_tunic" name="Zora Tunic" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'TunicGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
