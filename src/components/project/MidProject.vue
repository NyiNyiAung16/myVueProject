<template>
    <div class="imgControler" v-if="this.viewPhoto">
        <img src="https://shorturl.at/ryBNQ" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/vASV1" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/aKOW8" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/fmHOS" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/ckquQ" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/cdHM5" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/adfjH" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/bhqK6" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/qszHV" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/aluW9" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/lBKO2" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/dqJX5" alt="img" width="200" height="300" class="photo">
        <img src="https://shorturl.at/BGOQW" alt="img" width="200" height="300" class="photo">
    </div>
    <div class="buttonController">
        <div v-if="this.viewPhoto===false">
            <span class="text">If you want to see blackpink photo, just click open.</span>
            <button class="mg" @click="openPhoto" >open</button>
        </div>
        <div v-if="this.viewPhoto===true">
            <span class="text">If you wanna close photo , just click close.</span>
            <button class="mg" @click="closePhoto" >close</button>
        </div>
    </div>
</template>

<script>
export default {
    data(){
       return{
        viewPhoto:true
       }
    },
    methods:{
        openPhoto(){
            this.viewPhoto=true
        },
        closePhoto(){
            this.viewPhoto=false
        }
    }
}
</script>

<style scoped>
    .imgControler{
        display: flex;
        justify-content:space-evenly;
        flex-wrap: wrap;
    }
    .buttonController{
        text-align: center;
        margin-top: 20px;
    }
    .text{
        color: pink;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }
    .photo{
        border-radius: 17px;
        margin-bottom: 10px;
    }
    .mg{
        background-color: pink;
        border: 1px solid white;
        border-radius: 3px;
    }
</style>