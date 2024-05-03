<script setup>
import { onMounted, reactive, ref } from 'vue';

defineProps([
    "personagem"
])

</script>

<template>
    <div class="col">
        <div class="card m-3">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="personagem.image" class="img-fluid rounded-start" alt="...">
                </div>
                <div class="col-md-8" style="background-color: #45953b">
                    <div class="card-body" style="background-color: #45953b">
                        <h5 class="card-title">{{ personagem.name }}</h5>
                        <p class="card-text">
                        <strong>Status:</strong> {{ personagem.status }} <br>
                        <strong>Espécie:</strong> {{ personagem.species }} <br>
                        <strong>  Gênero:</strong> {{ personagem.gender }} <br>
                        <strong>Local:</strong> {{ personagem.location.name }} <br>
                        <strong> Total De episódios:</strong> {{ personagem.episode.length }} <br>
                        </p>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>