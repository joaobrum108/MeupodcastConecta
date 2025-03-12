<template>
  <div>
    <div v-if="videos.length === 0">Nenhum episódio disponível no momento.</div>

    <div v-else class="card-grid">
      <div v-for="episode in videos" :key="episode.id" class="card-container">
        <div class="card-image">
          <img
            :src="episode.thumbnail || 'placeholder.jpg'"
            alt="Thumbnail do episódio"
            loading="lazy"
          />
        </div>

        <div class="card-content">
          <h2>{{ episode.title }}</h2>
          <!-- <p class="description">{{ episode.description }}</p> -->
        </div>

        <div class="card-overlay">
          <button @click="handleClick(episode)">Acessar</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import { usePodcastStore } from "../stores";

const videos = ref([]);
const PodcastStore = usePodcastStore();

const SearchData = async () => {
  try {
    await PodcastStore.fetchEpisodes();
    videos.value = PodcastStore.episodes;
    console.log("Epsódios carregados com sucesso no card");
  } catch (error) {
    console.error("Erro ao buscar episódios:", error);
  }
};

let Pause;

onMounted(() => {
  SearchData();
  Pause = setInterval(() => {
    SearchData();
  }, 360000000);
  console.log("Componente montado no card");
});

onBeforeUnmount(() => {
  clearInterval(Pause);
  console.log("componente passou de 4 dias no card");
});

const handleClick = (episode) => {
  window.open(episode.link);
};
</script>

<style scoped>
h2 {
  font-family: "Poppins", sans-serif !important;
}
body {
  background-color: #121212;
  color: #ffffff;
  font-family: "Montserrat ", sans-serif;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.card-container {
  background-color: #1e1e1e;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  position: relative;
  cursor: pointer;
  height: auto;
  max-height: 100%;
}

.card-container:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.5);
}

.card-image img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
}

.card-content {
  padding: 16px;
}

.card-content h2 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 8px;
  color: #ffffff;
}

.card-content .description {
  font-size: 0.875rem;
  color: #b3b3b3;
  line-height: 1.5;
}

.card-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.card-container:hover .card-overlay {
  opacity: 1;
}

.card-overlay button {
  padding: 10px 20px;
  background-color: #bb86fc;
  color: #121212;
  border: none;
  border-radius: 6px;
  font-size: 0.875rem;
  font-weight: 500;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.card-overlay button:hover {
  background-color: #9a67ea;
}

div[v-if] {
  text-align: center;
  font-size: 1rem;
  color: #b3b3b3;
  padding: 20px;
}

@media (max-width: 1024px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(1, 1fr);
  }

  .card-container {
    width: 100%;
  }
}
</style>
