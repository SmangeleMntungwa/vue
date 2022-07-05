<template>
   
        <div class="cards">
        <h2> {{propertie.title}}</h2>
        <p> {{ propertie.area}}</p>
        <p>{{ propertie.bedrooms}}</p>
        </div>
    
</template>
<script>
export default {
    props:["propertie"]
}
</script>
<style>
    .cards {
        border: 2px solid;
        width: 300px;
    }
</style>