<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListaPersonagens from '@/components/ListaPersonagens.vue';

let personagens = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
    .then(response => response.json())
    .then(response => {
      personagens.value = response.results
    })
})

</script>

<template>
  <main>
    <div class="row row-cols-1 row-cols-md-2 g-4">
      <div v-for="personagem in personagens" :key="personagem.id">
        <ListaPersonagens :personagem="personagem" />
      </div>
    </div>
  </main>
</template>
