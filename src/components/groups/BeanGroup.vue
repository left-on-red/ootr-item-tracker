<template>
    <ItemGroup single>
        <ItemTracker image="magic_bean" name="Magic Beans" :labels="['1', '2', '3', '4', '5', '6', '7', '8', '9', '10']" />
    </ItemGroup>
</template>

<script>
import ItemGroup from './../ItemGroup.vue';
import ItemTracker from './../ItemTracker.vue';

export default {
    name: 'BeanGroup',
    components: { ItemGroup, ItemTracker }
}
</script>
