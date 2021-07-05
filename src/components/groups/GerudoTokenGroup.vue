<template>
    <ItemGroup single>
        <ItemTracker image="gerudo_token" name="Gerudo Membership Card" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'GerudoTokenGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
