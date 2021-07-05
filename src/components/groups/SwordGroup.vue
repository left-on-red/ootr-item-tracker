<template>
    <ItemGroup row>
        <ItemTracker image="kokiri_sword" name="Kokiri Sword" />
        <ItemTracker image="master_sword" name="Master Sword" />
        <ItemTracker image="biggoron_sword" name="Biggoron Sword" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'SwordGroup',
    components: { ItemGroup, ItemTracker }
}
</script>