<template>
    <h1>Bios</h1>

    <!-- <button @click="alive=false">hide</button> -->


    <div v-if="alive">
        <div v-for="bio in bios" :key="bio.hairColor" class="font">
        <h3>Name - {{bio.name}}</h3>
        <h3>Age - {{bio.age}}</h3>
        <h3>Haircolor - {{bio.hairColor}}</h3>
        <h3>Bornyear  - {{bio.bornYear}}</h3><hr>
    </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            bios:[
                {
                    name:'nyinyi',
                    age:19,
                    hairColor:'black',
                    bornYear:2003
                },
                {
                    name:'aungaung',
                    age:23,
                    hairColor:'black',
                    bornYear:1998
                },
                {
                    name:'susu',
                    age:16,
                    hairColor:'black',
                    bornYear:2006
                }
            ],
            alive:true
        }
    }
}
</script>

<style>
    .font{
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }
</style>