<template>
    <ItemGroup row>
        <ItemTracker image="deku_shield" name="Deku Shield" />
        <ItemTracker image="hylian_shield" name="Hylian Shield" />
        <ItemTracker image="mirror_shield" name="Mirror Shield" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'ShieldGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
