<template>
    <div class="selezione">
        <select @change="$emit('select', selezioneGenere)" v-model="selezioneGenere">
            <option value="all">All</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="rock">Rock</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selezioneGenere: 'all',
        }
    }
}
</script>

<style lang="scss" scoped>
.selezione {
    display: flex;
    justify-content: center ;
}
</style>