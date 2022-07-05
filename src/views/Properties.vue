<template>
<h1> All Properties</h1>
<div class="card-display"> 
    <PropertyCard v-for="propertie in properties" :key="propertie.id" :propertie="propertie" />
        
    
</div>

</template>
<script>

import PropertyCard from '../components/PropertyCard.vue'

export default {
    components: {
        PropertyCard
    },
    data() {
        return{
            properties:[]
        }
    },
    mounted(){
        fetch("http://localhost:3000/properties")
        .then((res) => res.json()).then((data => this.properties= data))
        .catch(err => console.log(err.message))
    },
};

</script>
<style>
    

    .card-display {
display: flex;
justify-content: space-evenly;
flex-wrap: nowrap;
gap: 50px;
    }

</style>