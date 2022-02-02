<template>
  <div id="app">
    <header-box/>
    <select-box @select="selectGenre"/>
    <main-container :dischi="genere"/>
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'
import SelectBox from './components/SelectBox.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    MainContainer,
    SelectBox
  }, 
  data() {
    return {
      dischi: [],
      genere: [],
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.dischi= response.data.response
      this.genere= response.data.response
    })
  },

  methods:{
    selectGenre(genre) {
      this.genere = this.dischi.filter((generi) => {
        return generi.genre.toLowerCase() === genre || genre === 'all';
      })
    }
  }
}
</script>

<style lang="scss">
@import './style/main.scss'
</style>
