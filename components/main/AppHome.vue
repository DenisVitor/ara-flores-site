<template>
  <main class="main-flower">
    <section class="main-flower-section-one">
      <div class="main-flower-section-text">
        <h1>Olá, Seja bem vindo ao Ara Flores</h1>
        <p>Aqui você encontrará o melhor da região no quesito flores</p>
      </div>
      <ul class="main-flower-section-list">
        <li>
          <video autoplay loop muted src="public/media/videobgone.mp4"></video>
        </li>
        <li>
          <video autoplay loop muted src="public/media/videobgtwo.mp4"></video>
        </li>
        <li>
          <video
            autoplay
            loop
            muted
            src="public/media/videobgthree.mp4"
          ></video>
        </li>
      </ul>
    </section>
    <section
      ref="firstAnimated"
      data-active="firstActive"
      class="main-flower-sec deactive"
    >
      <hgroup class="main-flower-text">
        <h1>Confira Aqui, um pouco de nosso trabalho!</h1>
        <h3>Dê uma olhada em nossos variados buquês e coroas.</h3>
        <p>
          Encontre a flor perfeita para cada momento. Descubra nossa coleção
          exclusiva e surpreenda-se! Transforme seu ambiente com cores e aromas.
          Clique e encante-se!
        </p>
      </hgroup>
      <figure class="main-flower-slider">
        <Transition :name="transition" mode="out-in">
          <img
            :key="flowerList[index].name"
            :src="flowerList[index].image"
            :alt="flowerList[index].name"
          />
        </Transition>
        <figcaption>
          <p>{{ flowerList[index].name }}</p>
        </figcaption>
        <div class="main-flowers-slider-buttons">
          <div @click="prevFlower" title="Anterior">
            <svg
              viewBox="0 0 32 32"
              version="1.1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              xmlns:sketch="http://www.bohemiancoding.com/sketch/ns"
              fill="#000000"
            >
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></g>
              <g id="SVGRepo_iconCarrier">
                <title>arrow-left-circle</title>
                <desc>Created with Sketch Beta.</desc>
                <defs></defs>
                <g
                  id="Page-1"
                  stroke="none"
                  stroke-width="1"
                  fill="none"
                  fill-rule="evenodd"
                  sketch:type="MSPage"
                >
                  <g
                    id="Icon-Set"
                    sketch:type="MSLayerGroup"
                    transform="translate(-256.000000, -1087.000000)"
                    fill="currentColor"
                  >
                    <path
                      d="M279,1102 L268.414,1102 L272.536,1097.88 C272.926,1097.49 272.926,1096.86 272.536,1096.46 C272.145,1096.07 271.512,1096.07 271.121,1096.46 L265.464,1102.12 C265.225,1102.36 265.15,1102.69 265.205,1103 C265.15,1103.31 265.225,1103.64 265.464,1103.88 L271.121,1109.54 C271.512,1109.93 272.145,1109.93 272.536,1109.54 C272.926,1109.15 272.926,1108.51 272.536,1108.12 L268.414,1104 L279,1104 C279.552,1104 280,1103.55 280,1103 C280,1102.45 279.552,1102 279,1102 L279,1102 Z M272,1117 C264.268,1117 258,1110.73 258,1103 C258,1095.27 264.268,1089 272,1089 C279.732,1089 286,1095.27 286,1103 C286,1110.73 279.732,1117 272,1117 L272,1117 Z M272,1087 C263.164,1087 256,1094.16 256,1103 C256,1111.84 263.164,1119 272,1119 C280.836,1119 288,1111.84 288,1103 C288,1094.16 280.836,1087 272,1087 L272,1087 Z"
                      id="arrow-left-circle"
                      sketch:type="MSShapeGroup"
                    ></path>
                  </g>
                </g>
              </g>
            </svg>
            <h4>Anterior</h4>
          </div>
          <div @click="nextFlower" title="Próximo">
            <h4>Próximo</h4>
            <svg
              viewBox="0 0 32 32"
              version="1.1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              xmlns:sketch="http://www.bohemiancoding.com/sketch/ns"
              fill="#000000"
            >
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></g>
              <g id="SVGRepo_iconCarrier">
                <title>arrow-right-circle</title>
                <desc>Created with Sketch Beta.</desc>
                <defs></defs>
                <g
                  id="Page-1"
                  stroke="none"
                  stroke-width="1"
                  fill="none"
                  fill-rule="evenodd"
                  sketch:type="MSPage"
                >
                  <g
                    id="Icon-Set"
                    sketch:type="MSLayerGroup"
                    transform="translate(-308.000000, -1087.000000)"
                    fill="currentColor"
                  >
                    <path
                      d="M324,1117 C316.268,1117 310,1110.73 310,1103 C310,1095.27 316.268,1089 324,1089 C331.732,1089 338,1095.27 338,1103 C338,1110.73 331.732,1117 324,1117 L324,1117 Z M324,1087 C315.163,1087 308,1094.16 308,1103 C308,1111.84 315.163,1119 324,1119 C332.837,1119 340,1111.84 340,1103 C340,1094.16 332.837,1087 324,1087 L324,1087 Z M330.535,1102.12 L324.879,1096.46 C324.488,1096.07 323.855,1096.07 323.465,1096.46 C323.074,1096.86 323.074,1097.49 323.465,1097.88 L327.586,1102 L317,1102 C316.447,1102 316,1102.45 316,1103 C316,1103.55 316.447,1104 317,1104 L327.586,1104 L323.465,1108.12 C323.074,1108.51 323.074,1109.15 323.465,1109.54 C323.855,1109.93 324.488,1109.93 324.879,1109.54 L330.535,1103.88 C330.775,1103.64 330.85,1103.31 330.795,1103 C330.85,1102.69 330.775,1102.36 330.535,1102.12 L330.535,1102.12 Z"
                      id="arrow-right-circle"
                      sketch:type="MSShapeGroup"
                    ></path>
                  </g>
                </g>
              </g>
            </svg>
          </div>
        </div>
      </figure>
    </section>
    <section
      data-active="secondActive"
      class="main-flower-section-two deactive"
      ref="secondAnimated"
    >
      <div class="main-flower-section-text-two">
        <h1>Aqui, Você encontra de tudo!</h1>
        <p>
          Na nossa empresa, transformamos flores em verdadeiras obras de arte,
          trazendo beleza e emoção para cada ocasião. Elaboramos coroas de
          flores com detalhes minuciosos, perfeitas para celebrar momentos
          especiais. Desenvolvemos ornamentos exclusivos que adicionam um toque
          de elegância a qualquer ambiente. Cada arranjo é cuidadosamente
          planejado para transmitir a personalidade e o estilo do cliente. Nossa
          equipe é movida pela paixão em criar composições que surpreendem e
          encantam. Atendemos a eventos, casamentos, aniversários e diversas
          outras celebrações com criatividade. Descubra como nosso universo
          floral pode transformar seus momentos em memórias inesquecíveis!
        </p>
      </div>
    </section>
    <section
      ref="thirdAnimated"
      data-active="thirdActive"
      class="main-flower-sec-two deactive"
    >
      <div class="main-flower-text-two">
        <hgroup class="main-flower-title-line">
          <span class="line"></span>
          <h1>Galeria</h1>
          <span class="line"></span>
        </hgroup>
        <NuxtLink to="/gallery">
          <button>Veja Agora</button>
        </NuxtLink>
        <p>
          Se gostou do nosso trabalho, venha conferir todos os frutos de nosso
          serviço!
        </p>
      </div>
      <div class="main-flower-marquee">
        <NuxtMarquee :gradient="true">
          <img
            v-for="(item, index) in flowerList"
            :src="item.image"
            :alt="item.name"
            :key="index"
          />
        </NuxtMarquee>
      </div>
    </section>
    <section
      class="main-flower-section-three deactive"
      data-active="fourthActive"
      ref="fourthAnimated"
    >
      <div class="main-flower-section-text-three">
        <h1>Venha nos visitar</h1>
        <p>e conferir nosso trabalho em primeira mão.</p>
        <sub>1387 R. Expedicionário Brasileiro</sub>
        <sub>Arapiraca, Alagoas</sub>
      </div>
      <img src="public\logo\location.png" alt="image-location" />
    </section>
    <section
      class="main-flower-sec-three deactive"
      data-active="fifthActive"
      ref="fifthAnimated"
    >
      <div class="main-flower-form">
        <div class="main-flower-form-inner">
          <label><span>Nome: </span><input type="text" name="" /></label>
          <label><span>Email: </span><input type="text" name="" /></label>
          <label><span>Endereço: </span><input type="text" name="" /></label>
          <label><span>Telefone: </span><input type="text" name="" /></label>
          <label>
            <span>Mensagem: </span>
            <textarea name="" id="" cols="30" rows="10"></textarea>
          </label>
        </div>
        <button>Enviar</button>
      </div>
      <div class="main-flower-text-three">
        <h1>Entre em contato já!</h1>
        <p>Não perca mais tempo e solicite já seu orçamento</p>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";
import { flowerList } from "../../server/mock/flowerList";

const index = ref(0);
const transition = ref("slide-forward");

const firstAnimated = ref<HTMLDivElement | null>(null);
const secondAnimated = ref<HTMLDivElement | null>(null);
const thirdAnimated = ref<HTMLDivElement | null>(null);
const fourthAnimated = ref<HTMLDivElement | null>(null);
const fifthAnimated = ref<HTMLDivElement | null>(null);

const nextFlower = () => {
  transition.value = "slide-forward";
  index.value = (index.value + 1) % flowerList.length;
};

const prevFlower = () => {
  transition.value = "slide-backward";
  index.value = (index.value - 1 + flowerList.length) % flowerList.length;
};

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          const activeClass = entry.target.getAttribute("data-active");
          if (activeClass) {
            entry.target.classList.add(activeClass);
          }
          observer.unobserve(entry.target);
        }
      });
    },
    { threshold: 0.5 }
  );
  if (firstAnimated.value) observer.observe(firstAnimated.value);
  if (secondAnimated.value) observer.observe(secondAnimated.value);
  if (thirdAnimated.value) observer.observe(thirdAnimated.value);
  if (fourthAnimated.value) observer.observe(fourthAnimated.value);
  if (fifthAnimated.value) observer.observe(fifthAnimated.value);
});
</script>

<style src="./AppHomeStyle.less"></style>
