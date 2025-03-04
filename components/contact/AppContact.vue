<template>
  <main class="main-contact">
    <section class="main-contact-title">
      <div class="main-contact-title-text">
        <h1>Contato</h1>
        <p>Venha nos visitar ou entre em contato conosco</p>
      </div>
    </section>
    <section class="main-contact-sec-one">
      <div class="main-contact-sec-one-location">
        <h1>Localização e contato</h1>
        <div class="main-contact-sec-one-location-subtext">
          <p>(82)99626-9107</p>
          <p>1387 R. Expedicionário Brasileiro</p>
          <p>Cemitério Pio XII - Baixa Grande, Arapiraca - AL</p>
        </div>
      </div>
      <figure class="main-contact-sec-one-image">
        <img src="public\logo\location.png" alt="image-location" />
      </figure>
    </section>
    <section class="main-contact-sec-two">
      <div class="main-contact-sec-two-text">
        <h1>Entre em contato já!</h1>
        <p>Não perca mais tempo e solicite já seu orçamento</p>
      </div>
      <div class="main-contact-sec-two-form">
        <div class="main-contact-form-inner">
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
    </section>
  </main>
</template>
<style src="./AppContactStyle.less"></style>
<script setup lang="ts">
const isOpen = ref(false);
</script>
