<template>
    <div class="dischi-box">
        <img :src="disco.poster" alt="">
        <p class="transform">{{disco.title}}</p>
        <p> {{disco.author}} </p>
        <p> {{disco.year}} </p>
    </div>
</template>

<script>
export default {
    props: {
        disco: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/dischi-box.scss'
</style>