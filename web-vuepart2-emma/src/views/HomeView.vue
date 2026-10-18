<script setup>
import { ref } from 'vue'

const email = ref('')
const formMessage = ref('En subscriure’t, acceptes rebre la newsletter de MALVA.')
const isSuccess = ref(false)

function handleSubscribe() {
  if (email.value) {
    formMessage.value = "Gràcies per l'interès! La subscripció de MALVA estarà disponible ben aviat."
    isSuccess.value = true
    email.value = ''
  }
}
</script>

<template>
  <main>
    <!-- Secció Hero / Portada -->
    <section class="hero" aria-labelledby="hero-title">
      <img
        class="hero-image"
        src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=2200&q=88"
        alt="Model amb un look de tardor en una ciutat"
      />
      <div class="hero-shade"></div>
      <div class="hero-topline">
        <span>EL NOU NUMERO</span>
        <span>01 — 04</span>
      </div>
      <div class="hero-copy">
        <p class="eyebrow">TARDOR / HIVERN 26</p>
        <h1 id="hero-title">Vesteix<br />el teu <em>moment.</em></h1>
        <p class="hero-description">Menys normes. Més tu. La nova manera de mirar la moda comença aquí.</p>
        <a class="round-link" href="#tendencies" aria-label="Descobreix les tendències">
          <span>Descobreix<br />la història</span><b aria-hidden="true">↘</b>
        </a>
      </div>
      <div class="hero-caption"><span>01 / PORTADA</span><span>Fotografia: Júlia Serra</span></div>
    </section>

    <!-- Manifest Ticker -->
    <section class="ticker" aria-label="Manifest MALVA">
      <div class="ticker-track">
        <span>LA TEVA MODA, LES TEVES REGLES</span><i>✳</i>
        <span>LA TEVA MODA, LES TEVES REGLES</span><i>✳</i>
        <span>LA TEVA MODA, LES TEVES REGLES</span><i>✳</i>
      </div>
    </section>

    <!-- Secció Tendències -->
    <section class="section trends-section" id="tendencies">
      <div class="section-heading">
        <div>
          <p class="eyebrow">EL RADAR MALVA · 03 MIN DE LECTURA</p>
          <h2>Ara mateix <em>ens posem…</em></h2>
        </div>
        <a class="text-link" href="#histories">Veure totes les tendències <span>↗</span></a>
      </div>
      <div class="trend-grid">
        <article class="trend-card trend-card-large">
          <a class="image-link" href="#histories" aria-label="Llegir sobre el vermell cirera">
            <img src="https://images.unsplash.com/photo-1551232864-3f0890e580d9?auto=format&fit=crop&w=1100&q=85" alt="Detall d'un look vermell intens" loading="lazy" />
            <span class="image-index">01</span>
          </a>
          <div class="card-meta"><span>TENDÈNCIA</span><span>4 MIN</span></div>
          <h3>Vermell cirera: el color que no demana permís</h3>
          <p>Un toc, un total look o aquella bossa que ho canvia tot.</p>
        </article>
        <article class="trend-card">
          <a class="image-link" href="#histories" aria-label="Llegir sobre la moda pre-loved">
            <img src="https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=900&q=85" alt="Estil de carrer amb una jaqueta oversize" loading="lazy" />
            <span class="image-index">02</span>
          </a>
          <div class="card-meta"><span>ESTIL SOSTENIBLE</span><span>6 MIN</span></div>
          <h3>Pre-loved, però que sembli molt teu</h3>
          <p>Trobar tresors també és una forma de tenir estil.</p>
        </article>
        <article class="trend-card">
          <a class="image-link" href="#histories" aria-label="Llegir sobre el nou uniforme">
            <img src="https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=900&q=85" alt="Dues amigues passejant amb looks urbans" loading="lazy" />
            <span class="image-index">03</span>
          </a>
          <div class="card-meta"><span>GUIA D'ESTIL</span><span>5 MIN</span></div>
          <h3>El nou uniforme: bàsics amb actitud</h3>
          <p>Les peces de sempre, combinades com mai.</p>
        </article>
      </div>
    </section>

    <!-- Secció Històries -->
    <section class="feature-story" id="histories">
      <div class="feature-image">
        <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=1300&q=88" alt="Retrat natural d'una jove creativa" loading="lazy" />
        <span class="feature-stamp">GENT<br />REAL<br />✳</span>
      </div>
      <div class="feature-copy">
        <p class="eyebrow">GENT MALVA · 8 MIN DE LECTURA</p>
        <h2>“No em vesteixo per encaixar. Em vesteixo per <em>sortir.”</em></h2>
        <p class="feature-description">La dissenyadora i DJ barcelonina Ona Pujol ens obre el seu armari —i ens explica per què el seu millor look és el que no havia planejat.</p>
        <a class="button-link" href="#estil">Llegeix l'entrevista <span>↗</span></a>
        <span class="feature-credit">TEXT: LAIA FONT · FOTOGRAFIA: NIL VIDAL</span>
      </div>
    </section>

    <!-- Secció Estil de carrer -->
    <section class="section street-section" id="estil">
      <div class="section-heading street-heading">
        <div>
          <p class="eyebrow">VIST AL CARRER · BARCELONA</p>
          <h2>El carrer <em>té la paraula.</em></h2>
        </div>
        <p class="street-intro">Looks reals, gent real, idees per endur-te. Aquest octubre, les millors referències no són a la passarel·la.</p>
      </div>
      <div class="street-grid">
        <figure class="street-photo street-one"><img src="https://images.unsplash.com/photo-1525507119028-ed4c629a60a3?auto=format&fit=crop&w=900&q=85" alt="Look urbà amb peces de tardor" loading="lazy" /><figcaption>GRÀCIA, 10:42 H</figcaption></figure>
        <figure class="street-photo street-two"><img src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=900&q=85" alt="Look creatiu fotografiat al carrer" loading="lazy" /><figcaption>EL BORN, 16:18 H</figcaption></figure>
        <figure class="street-photo street-three"><img src="https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=900&q=85" alt="Detall d'un estil personal i relaxat" loading="lazy" /><figcaption>POBLE-SEC, 12:06 H</figcaption></figure>
        <div class="street-note"><span>EL TEU LOOK<br />PODRIA SER<br /><em>EL SEGÜENT.</em></span><a href="mailto:hola@malva.cat">Envia'ns el teu <b>↗</b></a></div>
      </div>
    </section>

    <!-- Secció Newsletter -->
    <section class="newsletter" id="newsletter">
      <div class="newsletter-mark">M.</div>
      <div class="newsletter-copy">
        <p class="eyebrow">UNA CARTA QUE SÍ QUE OBRIRÀS</p>
        <h2>Una mica de MALVA<br />a la teva <em>inbox.</em></h2>
        <p>Tendències, idees i històries. Un cop per setmana, sense soroll.</p>
      </div>
      <form class="newsletter-form" @submit.prevent="handleSubscribe">
        <label for="email">EL TEU CORREU ELECTRÒNIC</label>
        <div class="input-row">
          <input 
            id="email" 
            type="email" 
            v-model="email" 
            placeholder="tu@exemple.com" 
            required 
          />
          <button type="submit" aria-label="Subscriure'm">↗</button>
        </div>
        <p class="form-message" :class="{ 'success': isSuccess }" aria-live="polite">
          {{ formMessage }}
        </p>
      </form>
    </section>
  </main>
</template>