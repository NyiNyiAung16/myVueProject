<template>

  <!-- <div class="main">
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
  </div> -->
  <Heading />
  <Mid/>
  <Bottom>
    <p>This is my first vue project And i think everybody likes it.</p>
  </Bottom>

  
</template>

<script>

import Heading from './components/project/HeadingProject.vue'
import Mid from './components/project/MidProject.vue'
import Bottom from './components/project/BottomProject.vue'

export default {
  name: 'App',
  components: {

    Heading,
    Mid,
    Bottom
  },
}
</script>

<style>
body{
  background-color: grey;
}
p{
  font-size: 20px;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  color:pink;
}
.changebc{
  background-color: red;
}
</style>
