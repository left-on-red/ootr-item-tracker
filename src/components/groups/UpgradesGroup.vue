<template>
    <ItemGroup row>
        <ItemTracker :images="['goron_bracelet', 'silver_gauntlets', 'gold_gauntlets']" :names="['Goron Bracelet', 'Silver Gauntlets', 'Gold Gauntlets']" />
        <ItemTracker :images="['silver_scale', 'gold_scale']" :names="['Silver Scale', 'Gold Scale']" />
        <ItemTracker :images="['adults_wallet', 'adults_wallet', 'giants_wallet', 'giants_wallet']" :names="['Childs Wallet', 'Adults Wallet', 'Giants Wallet', 'Tycoon Wallet']" :labels="['99', '200', '500', '999']" />
        <ItemTracker :images="['small_magic', 'large_magic']" :names="['Magic', 'Extended Magic']" />
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
