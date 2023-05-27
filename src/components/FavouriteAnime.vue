<template>
        <h3 v-if="this.favAnime===false">If you want to see favouite anime,click open.</h3>
        <h3 v-if="this.favAnime===true">If you want to hide favouite anime,click hide.</h3>

        <button @click="openAnime" v-if="this.favAnime===false" class="box">open</button>
        <button @click="closeAnime" v-if="this.favAnime===true" class="box">close</button>

        <h3 v-if="this.favAnime===true">If you want to delete favourite lists ,just click</h3>

    <div v-if="this.favAnime">
        <div v-for="serie in series" :key="serie.type" :class="{favSeries:serie.isfav}" @click="serie.isfav=false">
            <div v-if="serie.isfav">
                <h3>Anime Series name - {{serie.anime}}</h3>
                <h3>Anime Series rating - {{serie.rating}}</h3>
                <h3>Anime Series type - {{serie.type}}</h3>
                <img :src="serie.link" alt="photo" width="170" height="200">
            </div>
        </div>
    </div>

</template>

<script>
export default {
    data(){
        return{
           series:[
            {
                anime:"myheroacademia",
                rating:20,
                type:"fight secen",
                link:"https://shorturl.at/imno9",
                isfav:true
            },
            {
                anime:"onepiece",
                rating:30,
                type:"fight secen and comedy",
                link:"https://shorturl.at/jmEIX",
                isfav:true
            },
            {
                anime:"jujussukaisan",
                rating:26,
                type:"fight secen",
                link:"https://shorturl.at/iANW8",
                isfav:true
            },
            {
                anime:"overlord",
                rating:23,
                type:"fight secen",
                link:"https://shorturl.at/hBJP5",
                isfav:true
            }
           ],
           favAnime:false,
        }
    },
    methods:{
        openAnime(){
            this.favAnime=true
        },
        closeAnime(){
            this.favAnime=false
        }
    }
}
</script>

<style scoped>
    .favSeries{
        background-color: rgb(25, 147, 240);
        color: white;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }
    .box{
        background-color: rgba(38, 226, 18, 0.708);
        border: 1px solid gray;
        border-radius: 3px;
    }
</style>