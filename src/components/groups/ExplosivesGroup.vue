<template>
    <ItemGroup>
        <ItemTracker image="bomb" name="Bombs" :labels="['20', '30', '40']" />
        <ItemTracker image="bombchu" name="Bombchus" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'ExplosivesGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
