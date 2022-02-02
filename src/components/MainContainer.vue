<template>
    <div class="container">
        <dischi-box 
         v-for="(disco, index) in dischi"
        :key="index" 
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
.container {
    display: flex;
    flex-wrap: wrap;
    width: 1000px;
    margin: 0px auto;    
}
</style>