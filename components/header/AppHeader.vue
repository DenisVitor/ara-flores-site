<template>
  <header>
    <img
      class="free-flower-one"
      src="/public/logo/flowerbg.png"
      alt="flowerbg"
    />
    <img
      class="free-flower-two"
      src="/public/logo/flowerbgtwo.png"
      alt="flowerbg2"
    />
    <img
      class="free-flower-three"
      src="/public/logo/flowerbg3.png"
      alt="flowerbg3"
    />
    <NuxtLink to="/">
      <img
        class="header-image"
        src="/public/logo/file-removebg-preview.png"
        alt="Logo-ara-flores"
      />
    </NuxtLink>
    <img
      class="free-flower-four"
      src="/public/logo/flowerbgfour.png"
      alt="flowerbg"
    />
    <div class="header-text">
      <h1 class="header-text-big">Ara <span>Flores</span></h1>
      <p class="header-text-small">Floricultura</p>
    </div>
    <nav class="header-navigation">
      <ul class="header-navigation-list">
        <li class="header-navigation-item">
          <NuxtLink to="/"> Home </NuxtLink>
        </li>
        <li class="header-navigation-item">
          <NuxtLink to="/gallery">Galeria</NuxtLink>
        </li>
        <li class="header-navigation-item">
          <NuxtLink to="/contact"> Contato </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>
<style src="./AppHeaderStyle.less"></style>
