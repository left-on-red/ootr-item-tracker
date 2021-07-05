<template>
    <ItemGroup single>
        <ItemTracker image="letter" name="Ruto's Letter" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'LetterGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
