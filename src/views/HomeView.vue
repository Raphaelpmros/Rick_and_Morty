<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListComponents from '../components/ListComponents.vue';

let characters = reactive(ref([]));

onMounted(() => {
  fetchAllCharacters("https://rickandmortyapi.com/api/character");
});

async function fetchAllCharacters(url) {
  try {
    while (url) {
      const response = await fetch(url);
      const data = await response.json();
      characters.value = [...characters.value, ...data.results];
      url = data.info.next;
    }
  } catch (error) {
    console.error("Error fetching characters:", error);
  }
}
</script>


<template>
  <main>
    <div class="container">
      <div >
        

        <div >
          <div class="card-body row">
            <ListComponents v-for="character in characters" 
              :image="character.image" 
              :name="character.name" 
              :status="character.status" 
              :specie="character.species" 
              :gender="character.gender" 
              :episode="character.episode" 
              :location="character.location.name" 
            />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
