<template>
    <ItemGroup single>
        <ItemTracker
            :images="[
                'pocket_egg',
                'pocket_cucco',
                'cojiro',
                'odd_mushroom',
                'odd_potion',
                'poachers_saw',
                'broken_gorons_sword',
                'prescription',
                'eyeball_frog',
                'eye_drops',
                'claim_check'
            ]"
            
            :names="[
                'Pocket Egg',
                'Pocket Cucco',
                'Cojiro',
                'Odd Mushroom',
                'Odd Potion',
                'Poacher\'s Saw',
                'Broken Goron\'s Sword',
                'Prescription',
                'Eyeball Frog',
                'Eyedrops',
                'Claim Check'
            ]" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'ChildTradeGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
