<script setup>
import { ref } from 'vue'

const quinceañera = ref({
  nombre: "Getsemani Abigail",
  apellidos: "Sánchez Sánchez",
  fecha: "6 de Diciembre, 2025",
  hora: "16:00 hrs"
})

const misa = ref({
  iglesia: "Nuestra Señora del Carmen",
  direccion: "Buenavista esquina Olivos N°1, Colonia Loma Colorada 2da sección, Naucalpan de Juárez, Estado de México.",
  hora: "16:00 hrs",
  mapsLink: "https://maps.app.goo.gl/yR52HHYmp8MJubch8"
})

const evento = ref({
  salon: "Rancho Millán",
  direccion: "Francisco Villa #10, C.P. 53427, Naucalpan de Juárez, Estado de México.",
  hora: "17:30 hrs",
  mapsLink: "https://maps.app.goo.gl/ohiwqBFkTGHWLkbT8"
})
</script>

<template>
  <div class="landing-page">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-content">
        <h1 class="main-title">Mis Quince Años</h1>
        <img class="quinceanera-img" src="./assets/quinceanera.png" alt="Getsemani Abigail">
        <h2 class="name">{{ quinceañera.nombre }}</h2>
        <h3 class="lastname">{{ quinceañera.apellidos }}</h3>
        <div class="date-container">
          <p class="date">{{ quinceañera.fecha }}</p>
        </div>
        <div class="ornament">✨ 💫 ✨</div>
      </div>
    </section>

    <!-- Events Section - Combined -->
    <section class="events-section">
      <div class="container">
        <h3 class="section-title">Itinerario del Evento</h3>
        <div class="events-grid">
          <!-- Misa Card -->
          <div class="event-card misa-card">
            <div class="card-header">
              <div class="icon">⛪</div>
              <h4>Ceremonia Religiosa</h4>
            </div>
            <div class="card-body">
              <h5>{{ misa.iglesia }}</h5>
              <p class="address">{{ misa.direccion }}</p>
              <div class="time-badge">{{ misa.hora }}</div>
              <a :href="misa.mapsLink" target="_blank" class="maps-button">
                📍 Ver en Google Maps
              </a>
            </div>
          </div>

          <!-- Evento Card -->
          <div class="event-card fiesta-card">
            <div class="card-header">
              <div class="icon">🎉</div>
              <h4>Celebración</h4>
            </div>
            <div class="card-body">
              <h5>{{ evento.salon }}</h5>
              <p class="address">{{ evento.direccion }}</p>
              <div class="time-badge">{{ evento.hora }}</div>
              <a :href="evento.mapsLink" target="_blank" class="maps-button">
                📍 Ver en Google Maps
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- RSVP Section -->
    <section class="rsvp-section">
      <div class="container">
        <h3 class="section-title-footer">Confirma tu Asistencia</h3>
        <p class="rsvp-text">Tu presencia hará este día aún más especial</p>
        <div class="contact-info">
          <p>📞 Confirmar al: (562) 975-6313</p>
          <p>💌 WhatsApp: +52 562 975 6313</p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <p>"Gracias por acompañarme en este día tan especial"</p>
        <div class="ornament">💖</div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
</style>
