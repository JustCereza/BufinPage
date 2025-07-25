<script setup>
import { ref } from 'vue';
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';

// Importar imágenes
import bullseye from '../assets/bullseye.png';
import businessTeam from '../assets/business-team.jpg';
import decisionMaking from '../assets/decision-making.jpeg';
import mapWithPins from '../assets/map-with-pins.jpg';
import thinking from '../assets/thinking.jpg';
import vision from '../assets/vision.jpg';
import daiLogo from '../assets/Dai.jpg';
import binleyAnuncio from '../assets/binley-anuncio.png';
import img1 from '../assets/dai-modal-1.png';
import img2 from '../assets/dai-modal-2.png';
import img3 from '../assets/dai-modal-3.png';
import BufinLogo from '../assets/Bufin-Logo.png';

const showDAIModal = ref(false);
const showImageModal = ref(false);
</script>

<template>
  <Navbar />

  <div class="timeline-container">
    <h2 class="title">Sobre Nosotros</h2>

    <div class="timeline">
      <div class="timeline-item left">
        <div class="bubble">¿A qué nos dedicamos?</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="businessTeam" alt="Equipo de trabajo" class="timeline-img" />
          <p>Desarrollar servicios integrales conformados por empresas líderes en su actividad.</p>
          <i class="bi bi-building-fill icon"></i>
        </div>
      </div>

      <div class="timeline-item right">
        <div class="bubble">¿Qué logramos?</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="bullseye" alt="Logro diana" class="timeline-img" />
          <p>Logramos un concepto único en la cadena de logística, brindando soluciones integrales.</p>
          <p>Con más de 20 años de experiencia.</p>
          <i class="bi bi-bullseye icon"></i>
        </div>
      </div>

      <div class="timeline-item left">
        <div class="bubble">¿Qué generamos?</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="decisionMaking" alt="Toma de decisiones" class="timeline-img" />
          <p>Generamos ventajas competitivas para nuestros clientes, permitiendo una mejor toma de decisiones en comercio exterior.</p>
          <i class="bi bi-gear-fill icon"></i>
        </div>
      </div>

      <div class="timeline-item right">
        <div class="bubble">¿En dónde?</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="mapWithPins" alt="Mapa con pines" class="timeline-img" />
          <p>Presencia nacional e internacional, operando estratégicamente en los principales puertos y aduanas del país.</p>
          <i class="bi bi-geo-alt-fill icon"></i>
        </div>
      </div>

      <div class="timeline-item left">
        <div class="bubble">Nuestra Misión</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="thinking" alt="Persona con idea" class="timeline-img" />
          <p>Brindar servicios de comercio exterior con excelencia, integridad y compromiso, generando valor mediante soluciones efectivas e innovadoras.</p>
          <i class="bi bi-lightbulb-fill icon"></i>
        </div>
      </div>

      <div class="timeline-item right">
        <div class="bubble">Nuestra Visión</div>
        <div class="line"></div>
        <div class="content-block">
          <img :src="vision" alt="Camino al ocaso" class="timeline-img" />
          <p>Ser la consultora líder en comercio exterior en México, reconocida por nuestra calidad, experiencia y cobertura estratégica.</p>
          <i class="bi bi-eye-fill icon"></i>
        </div>
      </div>
    </div>
  </div>

    <div class="download-actions">
  <button class="dai-button" @click="showDAIModal = true">
    <span class="icon">📘</span>
    Ver información completa de DAI Despachos Aduanales Integrados
  </button>
</div>

    <transition name="fade-zoom">
      <div class="modal-backdrop" v-if="showDAIModal">
        <div class="modal-box">
          <div class="modal-content">
            <button class="close-button" @click="showDAIModal = false">✖</button>
            <div class="dai-logo-container">
              <img :src="daiLogo" alt="Logo DAI" class="dai-logo" />
            </div>
            <h2>📘 Despachos Aduanales Integrados (DAI)</h2>
            <h3>¿Quiénes somos?</h3>
            <ul>
              <li>Más que una agencia aduanal, DAI agrupa empresas líderes en logística y comercio exterior.</li>
              <li>Contamos con más de 20 años de experiencia y cobertura nacional e internacional.</li>
            </ul>

            <h3>Servicios destacados</h3>
            <ul>
              <li>Agencia Aduanal, logística, bodega en EUA, verificación en origen, unidad verificadora acreditada.</li>
              <li>Registros FDA, etiquetado, certificados de origen, capacitación y más.</li>
            </ul>
              <div class="dai-extra-images">
                <img :src="img1" alt="Ejemplo 1" class="dai-extra-img" />
              </div>
            <h3>Consultoría y cumplimiento</h3>
            <ul>
              <li>Trámites ante Economía, certificaciones IVA/IEPS, auditoría y control aduanero.</li>
            </ul>

            <h3>Contacto</h3>
            <ul>
              <li><strong>Teléfonos:</strong> (871) 213 4833 / (871) 213 2500 / 001 956 744 3348</li>
              <li><strong>Correos:</strong> jtorres@daiweb.mx / csandoval@daiweb.mx</li>
            </ul>
            <h3>Capacitación y servicios complementarios</h3>
    <ul>
      <li>BIN LEY y correlación aduanera, sistema de información y consulta básica.</li>
      <li>Pedimento aduanero, control de importaciones, manejo del activo fijo.</li>
      <li>Proyectos de exportación e importación.</li>
      <li>Certificación y manejo del anexo 24 y 30. Sistema Betta Global Systems.</li>
      <li>Importaciones temporales y definitivas. Especialización para obtener patente.</li>
      <li>Guía básica del exportador (Bancomext) y programa "Tú puedes exportar" (COMCE).</li>
    </ul>

            <div class="dai-extra-images">
                <img :src="img2" alt="Ejemplo 2" class="dai-extra-img" />
              </div>
            <div class="dai-extra-images">
                <img :src="img3" alt="Ejemplo 3" class="dai-extra-img" />
              </div>
    <h3>Servicios ampliados</h3>
    <ul>
      <li>Logística nacional e internacional. Revisión de origen y auditoría aduanera.</li>
      <li>Consultoría de comercio exterior, padrones, trámites ante Economía.</li>
      <li>Certificaciones IVA/IEPS. Unidad verificadora acreditada.</li>
      <li>Verificación de proveedores, seguros de mercancía, control de inventarios.</li>
    </ul>

            <div class="dai-extra-images">
                <img :src="BufinLogo" alt="Bufin Logo" class="dai-extra-img" />
              </div>
              
    <p style="margin-top: 1rem; font-style: italic; color: #1f3b73;">
      “Rapidez, costo y seguridad jurídica” en Despachos Aduanales Integrados.
    </p>

        <div class="binley-promo-container">
          <img
            :src="binleyAnuncio"
            alt="Promoción BIN LEY 2025"
            class="binley-promo-img"
            @click="showImageModal = true"
          />
          <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666;">Haz clic en la imagen para ampliarla</p>
        </div>
      </div>
    </div>
  </div>
</transition>

<transition name="fade-zoom">
  <div class="modal-backdrop" v-if="showImageModal" @click.self="showImageModal = false">
    <div class="image-modal-clean">
      <button class="close-button clean" @click="showImageModal = false">✖</button>
      <img :src="binleyAnuncio" alt="BIN LEY 2025" class="binley-full-image" />
    </div>
  </div>
</transition>




  <Footer />
</template>

<style scoped>
.timeline-container {
  background-color: #0a1f3c;
  color: #ffffff;
  padding: 2rem 1rem 6rem;
  font-family: 'Arial', sans-serif;
}

.title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 3.5rem;
  color: #f5b841;
}

.timeline {
  display: flex;
  flex-direction: column;
  gap: 4rem;
  position: relative;
  max-width: 1100px;
  margin: 0 auto;
}

.timeline::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  width: 2px;
  height: 100%;
  background-color: #44618d;
  transform: translateX(-50%);
  z-index: 0;
}

.timeline-item {
  display: flex;
  align-items: center;
  position: relative;
  gap: 1.5rem;
}

.timeline-item.left {
  flex-direction: row;
}

.timeline-item.right {
  flex-direction: row-reverse;
}

.bubble {
  background-color: #f5b841;
  color: #0a1f3c;
  border-radius: 999px;
  padding: 0.75rem 1.75rem;
  font-weight: 700;
  font-size: 1.1rem;
  border: 2px solid #fdf6e3;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
  white-space: nowrap;
  position: relative;
  z-index: 2;
}

.line {
  flex-shrink: 0;
  width: 40px;
  height: 3px;
  background-color: #f5b841;
  z-index: 1;
}

.content-block {
  background-color: #eaf0f6;
  color: #0a1f3c;
  padding: 1.75rem;
  border-radius: 1.5rem;
  max-width: 500px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
  position: relative;
  font-size: 1rem;
}

.content-block .icon {
  display: block;
  font-size: 2rem;
  margin-top: 1rem;
  color: #1f3b73;
  text-align: center;
}

/* Estilo mejorado para imágenes */
.timeline-img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 1.25rem;
  margin-bottom: 1rem;
  border: 2px solid #d6e1f2;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.25);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.timeline-img:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.35);
}

/* Responsive */
@media (max-width: 768px) {
  .timeline-item {
    flex-direction: column !important;
    align-items: flex-start !important;
  }

  .timeline-item.right {
    align-items: flex-end !important;
  }

  .line {
    width: 2px;
    height: 20px;
    background-color: #f5b841;
    margin: 0.5rem 0;
  }

  .bubble {
    margin-bottom: 0.75rem;
    font-size: 1rem;
  }

  .content-block {
    width: 100%;
  }
}
/* Modal backdrop */
.modal-backdrop {
  position: fixed;
  inset: 0;
  background-color: rgba(10, 31, 60, 0.85); /* azul oscuro translúcido */
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

/* Caja del modal */
.modal-box {
  background-color: transparent; 
  border-radius: 0;             
  padding: 0;                    
  max-width: 800px;
  width: 90%;
  overflow-y: auto;
  max-height: 100vh;
  animation: fadeInZoom 0.35s ease;
  display: flex;
  justify-content: center;
}


.close-button {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background-color: transparent;
  border: none;
  font-size: 1.5rem;
  color: #0a1f3c;
  cursor: pointer;
  transition: transform 0.2s ease, color 0.2s ease;
  z-index: 10;
}

.close-button:hover {
  color: #f5b841;
  transform: scale(1.2);
}


/* Contenido del modal */

.modal-content {
  position: relative;
  background-color: #ffffff;
  padding: 2rem;
  border-radius: 1.5rem;
  max-width: 700px;
  width: 100%;
  max-height: 85vh;
  overflow-y: auto;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
  color: #0a1f3c;
}


.modal-content h2 {
  color: #f5b841;
  font-size: 1.6rem;
  margin-bottom: 1rem;
  font-weight: bold;
}

.modal-content h3 {
  color: #1f3b73;
  font-size: 1.2rem;
  margin-top: 1.5rem;
  margin-bottom: 0.5rem;
}

.modal-content ul {
  padding-left: 1.2rem;
  list-style-type: disc;
  margin-bottom: 1.25rem;
}

.modal-content li {
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
}

.modal-content table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
  font-size: 0.95rem;
}

.modal-content th,
.modal-content td {
  border: 1px solid #ccc;
  padding: 0.6rem;
  text-align: left;
}

.modal-content th {
  background-color: #f5b841;
  color: #0a1f3c;
}

/* Animación entrada */
@keyframes fadeInZoom {
  0% {
    opacity: 0;
    transform: scale(0.85);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

/* Transición para Vue <transition> */
.fade-zoom-enter-active,
.fade-zoom-leave-active {
  transition: all 0.3s ease;
}

.fade-zoom-enter-from,
.fade-zoom-leave-to {
  opacity: 0;
  transform: scale(0.85);
}

.fade-zoom-enter-to,
.fade-zoom-leave-from {
  opacity: 1;
  transform: scale(1);
}

.download-actions {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 120px; 
  background-color:#0a1f3c;
}


.dai-button {
  background-color: #f5b841;
  color: #0a1f3c;
  font-weight: 700;
  font-size: 1rem;
  border: none;
  border-radius: 2rem;
  padding: 0.75rem 1.5rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
  display: flex;
  align-items: center;
  gap: 0.5rem;
  transition: all 0.25s ease;
  cursor: pointer;
}

.dai-button:hover {
  background-color: #f8c95a;
  transform: translateY(-2px);
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.35);
}

.dai-button .icon {
  font-size: 1.2rem;
}

.dai-logo-container {
  display: flex;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.dai-logo {
  width: 150px;
  height: auto;
  border-radius: 0.75rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.binley-promo-container {
  margin-top: 2rem;
  text-align: center;
}

.binley-promo-img {
  width: 100%;
  max-width: 550px;
  border-radius: 1rem;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease;
}

.binley-promo-img:hover {
  transform: scale(1.02);
}

.image-modal-box {
  position: relative;
  background-color: #ffffff;
  border-radius: 1rem;
  padding: 1rem;
  max-width: 90%;
  max-height: 90%;
  overflow: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
}

.full-image {
  max-width: 100%;
  max-height: 90vh;
  border-radius: 0.75rem;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
  object-fit: contain;
}

.image-modal-clean {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 95%;
  max-height: 95%;
}

.binley-full-image {
  max-width: 100%;
  max-height: 90vh;
  border-radius: 1rem;
  object-fit: contain;
  box-shadow: 0 6px 25px rgba(0, 0, 0, 0.6);
}

.close-button.clean {
  position: absolute;
  top: -2rem;
  right: -2rem;
  background-color: #ffffff;
  border-radius: 50%;
  font-size: 1.5rem;
  padding: 0.5rem 0.7rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
  color: #0a1f3c;
  cursor: pointer;
  border: none;
  z-index: 10;
  transition: all 0.3s ease;
}

.close-button.clean:hover {
  background-color: #f5b841;
  color: #0a1f3c;
  transform: scale(1.1);
}

.dai-extra-images {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  margin-top: 1rem;
}

.dai-extra-img {
  width: 100%;
  max-width: 300px;
  border-radius: 8px;
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.15);
  cursor: pointer;
  transition: transform 0.3s ease;
}

.dai-extra-img:hover {
  transform: scale(1.05);
}


</style>
