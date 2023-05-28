<template>
  <div class="main">
    <div>
      <img src="https://shorturl.at/ijFHT" alt="image here" width="70" height="60">
    </div>
    <div>
      <br>
      <span class="text">I love BlackPink And They are my angel.</span>
    </div>
    <div class="buttonController">
      <button class="mg" >Login In</button>
      <button class="mg">Sign Out</button>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  .main{
    display: flex;
    justify-content: space-around;
    margin-bottom: 20px;
  }
  .mg{
    margin-left: 20px;
    background-color: pink;
    border: 1px solid white;
    border-radius: 3px;
  }
  .text{
    font-size: 20px;
    color: pink;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  }
  .buttonController{
    padding-top: 20px;
  }
</style>