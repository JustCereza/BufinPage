<script setup>
import { ref } from 'vue'
import Navbar from '../components/Navbar.vue'
import Footer from '../components/Footer.vue'

// Estado del modal
const showImageModal = ref(false)
const currentImage = ref('')
const currentText = ref('')

// Datos para cada tarjeta
const auditoriaData = [
  {
    imagen: new URL('../assets/riesgos.jpg', import.meta.url).href,
    texto: 'Evaluamos procedimientos, documentación y cumplimiento para detectar posibles omisiones o errores que representen un riesgo para la empresa ante la autoridad aduanera.'
  },
  {
    imagen: new URL('../assets/documentos.png', import.meta.url).href,
    texto: 'Revisamos documentos clave como pedimentos, facturas y manifiestos para garantizar que todo esté conforme a los requerimientos legales y normativos.'
  },
  {
    imagen: new URL('../assets/diagrama-cliente.png', import.meta.url).href,
    texto: 'Identificamos desviaciones respecto a la normatividad vigente y brindamos recomendaciones puntuales para evitar sanciones o bloqueos.'
  },
  {
    imagen: new URL('../assets/hallazgos.jpg', import.meta.url).href,
    texto: 'Elaboramos un informe técnico que resume las inconsistencias detectadas, su impacto y las acciones correctivas sugeridas.'
  }
]

function openImageModal(index) {
  currentImage.value = auditoriaData[index].imagen
  currentText.value = auditoriaData[index].texto
  showImageModal.value = true
}

function closeImageModal() {
  showImageModal.value = false
}
</script>


<template>
  <Navbar />
  <div class="auditoria-container">
    <h2 class="title">Auditoría en Comercio Exterior</h2>

    <div class="cards-container">
      <!-- Tarjeta 1 -->
      <div class="card" @click="openImageModal(0)">
        <i class="bi bi-search icon"></i>
        <h3 class="card-title">Detección de riesgos</h3>
        <p class="card-text">Identificamos áreas vulnerables en tus procesos de importación y exportación, asegurando cumplimiento con la legislación aduanera vigente.</p>
      </div>

      <!-- Tarjeta 2 -->
      <div class="card" @click="openImageModal(1)">
        <i class="bi bi-file-earmark-check icon"></i>
        <h3 class="card-title">Revisión documental</h3>
        <p class="card-text">Auditamos pedimentos, facturas, y documentos aduanales para garantizar que todo esté en regla y evitar sanciones.</p>
      </div>

      <!-- Tarjeta 3 -->
      <div class="card" @click="openImageModal(2)">
        <i class="bi bi-shield-lock icon"></i>
        <h3 class="card-title">Cumplimiento normativo</h3>
        <p class="card-text">Aseguramos que tu empresa cumpla con las disposiciones legales, reduciendo el riesgo de multas o auditorías oficiales.</p>
      </div>

      <!-- Tarjeta 4 -->
      <div class="card" @click="openImageModal(3)">
        <i class="bi bi-bar-chart-line icon"></i>
        <h3 class="card-title">Informe de hallazgos</h3>
        <p class="card-text">Te entregamos un informe detallado con recomendaciones claras para optimizar tus procesos y mantenerte en regla.</p>
      </div>
    </div>

    <!-- Modal visual -->
    <transition name="fade">
      <div class="modal-backdrop" v-if="showImageModal">
        <div class="modal-box">
          <button class="modal-close" @click="closeImageModal">✖</button>
          <img :src="currentImage" alt="Detalle visual" class="modal-image" />
          <p class="modal-description">{{ currentText }}</p>
        </div>
      </div>
    </transition>
  </div>
  <Footer />
</template>

<style scoped>
.auditoria-container {
  background-color: #0e0e0e;
  color: white;
  padding: 3rem 1rem 6rem;
  font-family: 'Arial', sans-serif;
}

.title {
  text-align: center;
  font-size: 2.8rem;
  font-weight: bold;
  margin-bottom: 3rem;
  color: #ffffff;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
}

.card {
  color: #fff;
  border-radius: 1.5rem;
  padding: 2rem;
  width: 300px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
  cursor: pointer;
}

.card:nth-child(1) {
  background: linear-gradient(135deg, #4e9af1, #6acdfc);
}
.card:nth-child(2) {
  background: linear-gradient(135deg, #7c4dff, #b388ff);
}
.card:nth-child(3) {
  background: linear-gradient(135deg, #43cea2, #185a9d);
}
.card:nth-child(4) {
  background: linear-gradient(135deg, #f7971e, #ffd200);
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.4);
}

.card:nth-child(1) .icon { color: #d9ecff; }
.card:nth-child(2) .icon { color: #e3d7ff; }
.card:nth-child(3) .icon { color: #c8fff2; }
.card:nth-child(4) .icon { color: #fff5cc; }

.icon {
  font-size: 2.8rem;
  margin-bottom: 1rem;
}

.card-title {
  font-size: 1.4rem;
  font-weight: bold;
  margin-bottom: 0.75rem;
}

.card-text {
  font-size: 1rem;
  line-height: 1.5;
}

/* Modal personalizado */
.modal-backdrop {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.85);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 999;
}

.modal-box {
  background-color: #1e1e1e;
  border-radius: 16px;
  padding: 2rem;
  width: 90%;
  max-width: 600px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.6);
  position: relative;
  text-align: center;
  color: white;
}

.modal-close {
  position: absolute;
  top: 1rem;
  right: 1.5rem;
  background: none;
  border: none;
  font-size: 1.2rem;
  color: #aaa;
  cursor: pointer;
}

.modal-image {
  width: 100%;
  border-radius: 10px;
  max-height: 300px;
  object-fit: cover;
  margin-bottom: 1rem;
}

.modal-description {
  font-size: 1rem;
  line-height: 1.6;
  color: #e0e0e0;
}

/* Animación de entrada */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Responsive */
@media (max-width: 768px) {
  .cards-container {
    flex-direction: column;
    align-items: center;
  }

  .card {
    width: 100%;
    max-width: 90%;
  }
}
</style>
