<template>
  <div id="app">
    <header-box/>
    <main-container :dischi="dischi"/>
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderBox,
    MainContainer
  }, 
  data() {
    return {
      dischi: []
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.dischi= response.data.response
    })
  }
}
</script>

<style lang="scss">
@import './style/main.scss'
</style>
