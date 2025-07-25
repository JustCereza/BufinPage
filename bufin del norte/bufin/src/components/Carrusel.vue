<template>
  <div class="carousel-container my-4">
    <div class="container">
      <div class="card carousel-card animate__animated animate__fadeIn">
        <div class="card-body p-0">
          <div
            id="companyCarousel"
            class="carousel slide carousel-fade"
            data-bs-ride="carousel"
            data-bs-interval="3000"
            data-bs-pause="hover"
            aria-label="Carrusel de identidad de Bufin del Norte"
          >
            <!-- Indicadores -->
            <div class="carousel-indicators">
              <button type="button" data-bs-target="#companyCarousel" data-bs-slide-to="0" class="active" aria-label="Slide 1"></button>
              <button type="button" data-bs-target="#companyCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
              <button type="button" data-bs-target="#companyCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
              <button type="button" data-bs-target="#companyCarousel" data-bs-slide-to="3" aria-label="Slide 4"></button>
            </div>

            <!-- Slides -->
            <div class="carousel-inner">
              <div class="carousel-item active">
                <div class="carousel-content d-flex align-items-center justify-content-center">
                  <h2 class="display-1 fw-bold company-blue animate__animated animate__fadeInUp text-shadow">BN</h2>
                </div>
              </div>

              <div class="carousel-item">
                <div class="carousel-content d-flex align-items-center justify-content-center">
                  <img
                    src="/src/assets/bn.jpg"
                    alt="Logo circular azul de BN"
                    class="img-fluid carousel-logo animate__animated animate__fadeInUp"
                  />
                </div>
              </div>

              <div class="carousel-item">
                <div class="carousel-content d-flex align-items-center justify-content-center">
                  <img
                    src="/src/assets/bufin del norte.jpg"
                    alt="Imagen institucional de Bufin del Norte"
                    class="img-fluid rounded shadow-sm animate__animated animate__fadeInUp"
                  />
                </div>
              </div>

              <!-- Slide con imagen de BINLEY -->
              <div class="carousel-item">
                <div class="carousel-content d-flex align-items-center justify-content-center promo-container">
                  <router-link to="/programa" class="promo-link" aria-label="Ir a Programa Ley Aduanera">
                    <img
                      :src="binleySidePromo"
                      alt="BINLEY Correlación Aduanera Digital 2025"
                      class="img-fluid rounded shadow-sm animate__animated animate__fadeInUp promo-img"
                    />
                    <div class="promo-text">
                      <h3 class="glow-text">App BINLEY</h3>
                      <p>Correlación Aduanera</p>
                    </div>
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Flechas personalizadas -->
            <button class="custom-carousel-control prev" type="button" data-bs-target="#companyCarousel" data-bs-slide="prev">
              <span aria-hidden="true">←</span>
              <span class="visually-hidden">Anterior</span>
            </button>
            <button class="custom-carousel-control next" type="button" data-bs-target="#companyCarousel" data-bs-slide="next">
              <span aria-hidden="true">→</span>
              <span class="visually-hidden">Siguiente</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import binleySidePromo from '../assets/ProgramaLey.png'
</script>

<style scoped>
/* --- Container y Card --- */
.carousel-container {
  width: 100%;
}

.carousel-card {
  background-color: #ffffff;
  border: none;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.carousel-card:hover {
  transform: translateY(-3px);
}

/* --- Contenido del Slide --- */
.carousel-content {
  height: 400px;
  background-color: #ffffff;
  padding: 2rem;
  text-align: center;
  transition: opacity 0.5s ease-in-out;
}

.carousel-logo {
  height: 200px;
  width: 200px;
  border-radius: 50%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  object-fit: cover;
}

/* --- Slide BINLEY --- */
.promo-container {
  position: relative;
}

.promo-img {
  max-height: 100%;
  max-width: 100%;
  cursor: pointer;
  transition: transform 0.2s ease;
  border-radius: 12px;
}

.promo-img:hover {
  transform: scale(1.03);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
}

/* --- Texto superpuesto --- */
.promo-text {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(0, 0, 0, 0.7);
  padding: 1rem 2rem;
  border-radius: 12px;
  color: #fff;
  text-align: center;
  font-weight: bold;
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.8);
  animation: fadeInUp 1s ease;
}

.promo-text h3 {
  font-size: 1.4rem;
  margin: 0;
}

.promo-text p {
  font-size: 0.9rem;
  margin: 0;
  color: #fffbf2;
}

/* --- Glow Effect --- */
.glow-text {
  color: #ffdd57;
  text-shadow:
    0 0 5px #ffea9b,
    0 0 10px #ffd84a,
    0 0 20px #ffb400,
    0 0 30px #ff9f00;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  0% {
    text-shadow: 0 0 5px #ffea9b, 0 0 10px #ffd84a, 0 0 20px #ffb400, 0 0 30px #ff9f00;
  }
  100% {
    text-shadow: 0 0 10px #fff6d1, 0 0 20px #ffdc7a, 0 0 30px #ffc107, 0 0 40px #ffa000;
  }
}

/* --- Indicadores --- */
.carousel-indicators button {
  background-color: #0e4b6b;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  margin: 0 6px;
  border: none;
}

/* --- Botones Flecha --- */
.custom-carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: #0e4b6b;
  color: white;
  border: none;
  font-size: 1.5rem;
  padding: 0.5rem 1rem;
  border-radius: 50%;
  z-index: 10;
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
}

.custom-carousel-control:hover {
  transform: translateY(-50%) scale(1.1);
}

.custom-carousel-control.prev {
  left: 10px;
}

.custom-carousel-control.next {
  right: 10px;
}

/* --- Responsive --- */
@media (max-width: 768px) {
  .carousel-content {
    height: 300px;
    padding: 1rem;
  }

  .promo-text {
    font-size: 0.8rem;
    padding: 0.6rem 1rem;
  }

  .carousel-logo {
    height: 140px;
    width: 140px;
  }
}

@media (max-width: 480px) {
  .carousel-content {
    height: 250px;
  }

  .promo-text h3 {
    font-size: 1.1rem;
  }
}
</style>
