<script setup>
const character = defineProps(["image", "name", "status", "specie", "gender", "location", "episode"])

</script>

<template>
    <div class="col-md-4">
        <div class="card p-2 mb-3" >
            <img :src="character.image" >
            <p class="text-center">Name: {{ character.name }}</p>
            <p class="text-center">Status: {{ character.status }}</p>
            <p class="text-center">Specie: {{ character.specie }}</p>
            <p class="text-center">Gender: {{ character.gender }}</p>
            <p class="text-center">Episodes: {{ character.episode.length }}</p>
            <p class="text-center">Location: {{ character.location }}</p>
        </div>
    </div>    
</template>

<style>

</style>