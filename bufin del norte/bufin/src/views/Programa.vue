<script setup lang="ts">
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';
import { ref } from 'vue';

import binleySidePromo from '../assets/ProgramaLey.png';

const downloadApp = () => {
  window.open('https://bufinorte.com/LeyAduanera/', '_blank', 'noopener');
};

const showModal = ref(false);

const openModal = () => {
  showModal.value = true;
};

const closeModal = () => {
  showModal.value = false;
};
</script>

<template>
  <Navbar />
  <main class="download-container">
  <div class="download-columns">
    
    <section class="download-content">
      <!-- Título -->
      <h1 class="download-title">Ley Aduanera</h1>

      <!-- Logo -->
      <header class="logo-container">
        <div class="logo-content">
          <div class="logo-text">
            <span class="logo-main">BUFIN DEL NORTE</span>
            <span class="logo-sub">CONSULTORES DE COMERCIO EXTERIOR</span>
          </div>
        <div class="world-icon" aria-hidden="true">
            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="#0077b6" class="bi bi-globe" viewBox="0 0 16 16">
              <path d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8m7.5-6.923c-.67.204-1.335.82-1.887 1.855A7.97 7.97 0 0 0 5.145 4H7.5zM4.09 4a9.267 9.267 0 0 1 .64-1.539 6.7 6.7 0 0 1 .597-.933A7.025 7.025 0 0 0 2.255 4zm-.582 3.5c.03-.877.138-1.718.312-2.5H1.674a6.958 6.958 0 0 0-.656 2.5zM4.847 5a12.5 12.5 0 0 0-.338 2.5H7.5V5zM8.5 5v2.5h2.99a12.495 12.495 0 0 0-.337-2.5zM4.51 8.5a12.5 12.5 0 0 0 .337 2.5H7.5V8.5zm3.99 0V11h2.653c.187-.765.306-1.608.338-2.5zM5.145 12c.138.386.295.744.468 1.068.552 1.035 1.218 1.65 1.887 1.855V12zm.182 2.472a6.696 6.696 0 0 1-.597-.933A9.268 9.268 0 0 1 4.09 12H2.255a7.024 7.024 0 0 0 3.072 2.472M3.82 11a13.652 13.652 0 0 1-.312-2.5h-2.49c.062.89.291 1.733.656 2.5zm6.853 3.472A7.024 7.024 0 0 0 13.745 12H11.91a9.27 9.27 0 0 1-.64 1.539 6.688 6.688 0 0 1-.597.933M8.5 12v2.923c.67-.204 1.335-.82 1.887-1.855.173-.324.33-.682.468-1.068zm3.68-1h2.146c.365-.767.594-1.61.656-2.5h-2.49a13.65 13.65 0 0 1-.312 2.5zm2.802-3.5a6.959 6.959 0 0 0-.656-2.5H12.18c.174.782.282 1.623.312 2.5zM11.27 2.461c.247.464.462.98.64 1.539h1.835a7.024 7.024 0 0 0-3.072-2.472c.218.284.418.598.597.933zM10.855 4a7.966 7.966 0 0 0-.468-1.068C9.835 1.897 9.17 1.282 8.5 1.077V4z"/>
            </svg>
          </div>
        </div>
      </header>

      <!-- Caja de información -->
      <section class="info-box">
        <p class="info-text">
          Descarga nuestra <strong>Ley Aduanera</strong> y mantente al día con las disposiciones legales en comercio exterior. Herramienta esencial para importadores, exportadores y consultores.
        </p>
        <div class="download-icon-container" aria-hidden="true">
        </div>
      </section>

      <!-- Botones -->
      <div class="download-actions">
        <a href="https://bufinorte.com/LeyAduanera/LeyAduanera.zip" download class="download-button">
          📥 Descargar Ley Aduanera
        </a>
        <a href="https://bufinorte.com/LeyAduanera/" target="_blank" rel="noopener noreferrer" class="url-link">
          🔗 Ver en el navegador
        </a>     
      </div>


        <!-- Botón de Instrucciones -->
        <div class="download-actions">
          <button class="download-button secondary" @click="openModal">
            📋 Instrucciones
          </button>
        </div>

 <!--instrucciones -->
<transition name="fade-zoom">
  <div class="modal-backdrop" v-if="showModal">
    <div class="modal-box">
      <button class="close-button" @click="closeModal">✖</button>
      <div class="modal-content">
        <h2>📘 BINLEY Correlación Aduanera Digital 2025</h2>

        <h3>🔧 Instrucciones para descargar e instalar el programa</h3>

        <h4>✅ 1. Descarga del archivo</h4>
        <ul>
          <li>Haz clic en <strong>"Descargar LeyAduanera.zip"</strong>.</li>
          <li>Contiene todos los elementos necesarios para la instalación.</li>
        </ul>

        <h4>✅ 2. Extracción del contenido</h4>
        <ul>
          <li>Descomprime el archivo ZIP en una carpeta de tu elección.</li>
          <li>Es obligatorio antes de ejecutar la instalación.</li>
        </ul>

        <h4>✅ 3. Instalación del programa</h4>
        <ul>
          <li>Dentro de la carpeta extraída, ejecuta <code>setup.exe</code>.</li>
          <li>Esto abrirá el asistente de instalación.</li>
        </ul>

        <h4>✅ 4. Asistente de instalación</h4>
        <ul>
          <li>Sigue todos los pasos del asistente hasta completar la instalación.</li>
        </ul>

        <h4>✅ 5. Activación de la licencia</h4>
        <ul>
          <li>Una vez instalado, adquiere tu licencia de uso y activala.</li>
          <li>Requiere <strong>acceso a internet</strong>.</li>
        </ul>

        <h4>✅ 6. Confirmación de activación</h4>
        <ul>
          <li>Si se activa correctamente, el programa estará listo para usarse.</li>
        </ul>

        <h4>📞 Información de contacto para adquirir una licencia</h4>
        <ul>
          <li><strong>Teléfonos:</strong> 871 2134833 / 871 2197093</li>
          <li><strong>Correo:</strong> <a href="mailto:icomtradesol@gmail.com">icomtradesol@gmail.com</a></li>
        </ul>

        <h4>📝 Resumen en pasos</h4>
        <table class="modal-table">
          <thead>
            <tr>
              <th>Paso</th>
              <th>Acción</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>1</td><td>Descargar <code>LeyAduanera.zip</code></td></tr>
            <tr><td>2</td><td>Extraer el archivo ZIP en una carpeta</td></tr>
            <tr><td>3</td><td>Ejecutar <code>setup.exe</code> para instalar</td></tr>
            <tr><td>4</td><td>Seguir el asistente de instalación</td></tr>
            <tr><td>5</td><td>Activar la licencia (requiere internet)</td></tr>
            <tr><td>6</td><td>Si se activa, el programa estará listo para usarse</td></tr>
            <tr><td>7</td><td>Adquirir licencia por teléfono o correo</td></tr>
          </tbody>
        </table>
      </div>
                    <!-- Dentro del modal -->
      <div class="modal-content">
        <h2>📘 Tutorial Ley Aduanera</h2>
        <p>Puedes visualizar el tutorial aquí mismo o abrirlo en una pestaña nueva para mayor comodidad.</p>

        <!-- Visor integrado -->
        <iframe 
          src="/binley-tutorial.pdf" 
          width="100%" 
          height="500px" 
          style="border:none; border-radius: 0.5rem;">
        </iframe>

        <!-- Botón para abrir en otra pestaña -->
        <div style="margin-top: 1rem; text-align:center;">
          <a href="/binley-tutorial.pdf" target="_blank" class="download-button secondary">
            🔗 Abrir en nueva pestaña
          </a>
        </div>
      </div>

    </div>
  </div>
</transition>

    </section>



  </div>
</main>

  <Footer />
</template>

<style scoped>
.download-container {
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to bottom right, #003049, #191919);
  padding: 2rem 1rem;
  min-height: 100vh;
}

.download-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 540px;
  width: 100%;
  gap: 2rem;
}

.download-title {
  color: #ffffff;
  font-size: 2.2rem;
  font-weight: 800;
  text-align: center;
  background: linear-gradient(to right, #00b4d8, #90e0ef);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.logo-container {
  background-color: #e0f7ff;
  border-radius: 1rem;
  padding: 1.2rem 1.5rem;
  width: 100%;
  box-shadow: 0 4px 12px rgba(0, 180, 216, 0.2);
}

.logo-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.logo-text {
  text-align: center;
  flex: 1;
}

.logo-main {
  display: block;
  color: #0077b6;
  font-weight: 700;
  font-size: 1rem;
}

.logo-sub {
  display: block;
  color: #005377;
  font-size: 0.7rem;
}

.world-icon {
  animation: rotate 12s linear infinite;
}

@keyframes rotate {
  from { transform: rotate(0); }
  to { transform: rotate(360deg); }
}

.info-box {
  background-color: #ffffff;
  border-left: 6px solid #00b4d8;
  border-radius: 1rem;
  padding: 1.5rem;
  text-align: center;
  color: #333;
  width: 100%;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.info-text {
  font-size: 1rem;
  line-height: 1.6;
}

.download-icon-container {
  margin-top: 1rem;
  display: flex;
  justify-content: center;
}

.download-icon {
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-8px); }
}

.download-actions {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.download-button {
  background: linear-gradient(to right, #00b4d8, #48cae4);
  color: #ffffff;
  padding: 0.75rem 2rem;
  font-size: 1rem;
  border: none;
  border-radius: 2rem;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: bold;
  width: 100%;
  max-width: 300px;
}

.download-button:hover {
  background: linear-gradient(to right, #48cae4, #00b4d8);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(72, 202, 228, 0.3);
}

.url-link {
  color: #ade8f4;
  font-size: 0.9rem;
  text-decoration: underline;
  transition: color 0.3s ease;
}

.url-link:hover {
  color: #ffffff;
}

@media (prefers-reduced-motion: reduce) {
  .world-icon,
  .download-icon {
    animation: none !important;
  }
}

@media (max-width: 576px) {
  .download-title {
    font-size: 1.6rem;
  }
  .info-text {
    font-size: 0.95rem;
  }
  .download-button,
  .logo-container {
    width: 90%;
  }
}
.secondary {
  background: linear-gradient(to right, #caf0f8, #90e0ef);
  color: #003049;
}

.secondary:hover {
  background: linear-gradient(to right, #90e0ef, #48cae4);
}

.modal-backdrop {
  position: fixed;
  inset: 0;
  background-color: rgba(0, 0, 0, 0.65);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.modal-box {
  background: #ffffff;
  border-radius: 1rem;
  max-width: 600px;
  padding: 2rem;
  position: relative;
  box-shadow: 0 0 20px rgba(0, 180, 216, 0.4);
  overflow-y: auto;
  max-height: 90vh;
  width: 90%;
}

.modal-content {
  font-size: 0.95rem;
  line-height: 1.6;
  color: #333;
}

.modal-content ul {
  padding-left: 1.2rem;
  margin-bottom: 1rem;
  list-style-type: disc;
}

.modal-content h2 {
  color: #0077b6;
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

.modal-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
}

.modal-table th,
.modal-table td {
  border: 1px solid #ccc;
  padding: 0.5rem;
  font-size: 0.9rem;
  text-align: left;
}

.modal-table th {
  background-color: #e0f7ff;
}

.close-button {
  position: absolute;
  top: 0.8rem;
  right: 1rem;
  font-size: 1.2rem;
  background: none;
  border: none;
  cursor: pointer;
  color: #666;
}

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

.modal-box {
  animation: fadeInZoom 0.3s ease-out;
}

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

.download-columns {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  gap: 3rem;
  max-width: 1200px;
  width: 100%;
}

.download-content {
  flex: 1;
  max-width: 540px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.promo-aside {
  flex: 100%;
  max-width: 420px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.promo-aside-img {
  width: 120%;
  max-width: 120%;
  border-radius: 1rem;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
}

@media (max-width: 768px) {
  .promo-aside {
    display: none;
  }
}


</style>
