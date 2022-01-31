<template>
    <div>
        <dischi-box
         v-for="disco in dischi"
        :key="disco.id" 
        :disco="disco"/>
    </div>
</template>

<script>
import DischiBox from './DischiBox.vue'

export default {
    components: {
        DischiBox
    },
    props: {
        dischi: Array,
    }
}
</script>

<style lang="scss" scoped>

</style>