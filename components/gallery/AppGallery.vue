<template>
  <main class="flower-gallery">
    <section class="flower-gallery-sec-one">
      <div class="flower-gallery-sec-one-text">
        <h1>Galeria</h1>
        <p>Veja nosso trabalho e faça seu pedido já.</p>
      </div>
    </section>
    <section class="flower-gallery-sec-two">
      <ul class="flower-gallery-sec-two-list">
        <li v-for="(flower, index) in flowerGalleryList" :key="flower.id">
          <img :src="flower.image" :alt="flower.name" :key="flower.id" />
          <h4 @click="openModal(flower)">
            {{ flower.name }}
          </h4>
          <p>{{ flower.type }}</p>
        </li>
      </ul>
    </section>
  </main>
  <div class="main-gallery-overlay" v-if="showModal" @click.self="closeModal">
    <div class="main-gallery-modal">
      <h2 class="main-gallery-modal-close" @click="closeModal">X</h2>
      <img :src="selectedItem?.image" :alt="selectedItem?.name" />
      <div class="main-gallery-modal-inner">
        <h1>{{ selectedItem?.name }}</h1>
        <h4>
          <q
            ><i>
              {{ selectedItem?.description }}
            </i>
          </q>
        </h4>
        <div>
          <h5>Type:</h5>
          <p>{{ selectedItem?.type }}</p>
        </div>
        <div>
          <h5>Flores:</h5>
          <p>{{ formattedNames }}</p>
        </div>
      </div>
      <button>Solicite já o seu orçamento</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { flowerGalleryList } from "~/mock/flowerGalleryList";
import type { GalleryFlowers } from "~/mock/flowerGalleryList";

const selectedItem = ref<GalleryFlowers | null>(null);
const showModal = ref(false);

const openModal = (item: GalleryFlowers) => {
  selectedItem.value = item;
  showModal.value = true;
};

const closeModal = () => {
  showModal.value = false;
};

const formattedNames = computed(() => {
  if (!selectedItem.value) return "";

  const namesList = selectedItem.value.flowers;
  if (namesList.length === 0) return "";
  if (namesList.length === 1) return namesList[0];

  return `${namesList.slice(0, -1).join(", ")} e ${
    namesList[namesList.length - 1]
  }`;
});

const handleKeydown = (event: KeyboardEvent): void => {
  if (event.key === "Escape") {
    closeModal();
  }
};

watch(showModal, (isOpen) => {
  if (isOpen) {
    window.addEventListener("keydown", handleKeydown);
  } else {
    window.removeEventListener("keydown", handleKeydown);
  }
});
</script>
<style src="./AppGalleryStyle.less"></style>
