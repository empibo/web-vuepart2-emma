<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value
}

function closeMenu() {
  isMenuOpen.value = false
}
</script>

<template>
  <div id="top">
    <!-- Anunci a la part superior -->
    <div class="announcement">
      <span>LA MODA CANVIA. TU POSES LES REGLES.</span>
      <span class="announcement-note">Núm. 08 · Barcelona, octubre 2026</span>
    </div>

    <!-- Capçalera amb menú desplegable reactiu -->
    <header class="site-header">
      <button 
        class="menu-toggle" 
        :aria-label="isMenuOpen ? 'Tancar el menú' : 'Obrir el menú'" 
        :aria-expanded="isMenuOpen"
        @click="toggleMenu"
      >
        <span></span><span></span>
      </button>

      <nav class="main-nav" :class="{ 'is-open': isMenuOpen }" aria-label="Navegació principal">
        <a href="#tendencies" @click="closeMenu">Tendències</a>
        <a href="#histories" @click="closeMenu">Històries</a>
        <a href="#estil" @click="closeMenu">Estil de carrer</a>
      </nav>

      <router-link class="wordmark" to="/" aria-label="MALVA, inici">MALVA<span>®</span></router-link>

      <div class="header-actions">
        <a href="#newsletter">Subscriu-te <span aria-hidden="true">↗</span></a>
        <a class="search-button" href="#tendencies" aria-label="Explorar tendències">
          <svg viewBox="0 0 24 24" aria-hidden="true"><circle cx="10.8" cy="10.8" r="6.8"></circle><path d="m16 16 5 5"></path></svg>
        </a>
      </div>
    </header>

    <!-- Vista principal de la pàgina -->
    <router-view />

    <!-- Peu de pàgina (Footer) -->
    <footer class="site-footer">
      <router-link class="footer-wordmark" to="/">MALVA<span>®</span></router-link>
      <p>Moda per a la vida real. Fet a Barcelona, per a tothom.</p>
      <div class="footer-bottom">
        <span>© MALVA 2026</span>
        <div>
          <a href="#newsletter">Instagram ↗</a>
          <a href="mailto:hola@malva.cat">Contacte</a>
          <a href="#top">Privacitat</a>
        </div>
        <span>AMB INTENCIÓ, SEMPRE.</span>
      </div>
    </footer>
  </div>
</template>
