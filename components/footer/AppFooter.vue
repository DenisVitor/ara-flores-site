<template>
  <footer>
    <img
      class="footer-image"
      src="/public/logo/file-removebg-preview.png"
      alt="Logo-ara-flores"
    />
    <ul class="footer-list">
      <li class="footer-item-first">Páginas</li>
      <NuxtLink to="/">
        <li class="footer-item">Home</li>
      </NuxtLink>
      <NuxtLink to="/gallery">
        <li class="footer-item">Galeria</li>
      </NuxtLink>
      <NuxtLink to="/contact">
        <li class="footer-item">Contato</li>
      </NuxtLink>
    </ul>
    <div class="footer-status">
      <h4>Ara flores Floricultura</h4>
      <p>Ornamentações, Coroas de flores, Centros de mesa, Arranjos e Buquês</p>
      <p>Tudo em um só lugar</p>
      <p>(82)99626-9107</p>
      <p>Cemitério Pio XII - Baixa Grande, Arapiraca - AL</p>
    </div>
  </footer>
</template>
<style src="./AppFooterStyle.less"></style>
