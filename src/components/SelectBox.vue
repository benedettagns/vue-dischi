<template>
    <div>
        <select @change="$emit('select', selezioneGenere)" v-model="selezioneGenere">
            <option value="">All</option>
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
            selezioneGenere= '',
        }
    }
}
</script>

<style lang="scss" scoped>

</style>