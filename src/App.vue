<template>

  <div class="main">
    <div>
      <h3 v-if="this.hide===false">If you want to see bio,click open</h3>
      <h3 v-if="this.hide===true">If you want to hide bio,click hide.</h3>
      <button @click="openBio" v-if="this.hide===false" class="clickBox">open</button>
      <button @click="hideBio" v-if="this.hide==true" class="clickBox">hide</button>
 
    <div v-if="hide">
      <bio/>
      </div>
    </div>


    <div>
      <Anime/>
    </div>
  </div>

  
</template>

<script>
import Bio from './components/bio.vue'
import Anime from './components/FavouriteAnime.vue'

export default {
  name: 'App',
  components: {
    Bio,
    Anime
  },
  data(){
    return{
        hide:false,
    }
  },
  methods:{
    hideBio(){
        this.hide=false,
        this.anime=false
    },
    openBio(){
      this.hide=true,
      this.anime=true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.clickBox{
  background-color: rgba(38, 226, 18, 0.708);
  border: 1px solid gray;
  border-radius: 3px;
}
.main{
  display: flex;
  justify-content: space-evenly;
}
h3{
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
}
</style>
