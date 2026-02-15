# Netflix Clone Template

## Descripción
Este template recrea la experiencia inmersiva de Netflix, utilizando un tema oscuro (`dark mode`), un banner de video hero a pantalla completa y múltiples carruseles horizontales para categorías de contenido. Se enfoca en la visualización de medios y una navegación minimalista.

## Estructura Clave
- **Hero Banner:** Usa un contenedor `.large-height` con un video `.responsive` de fondo y contenido posicionado absolutamente (`absolute.left.middle-align`).
- **Top Navigation:** Usa `nav.top.top-shadow` con texto blanco. Implementa un menú desplegable para móvil (`menu`) y botones directos para desktop (`l`).
- **Content Sections:** Organizadas por IDs (`#series`, `#movies`) para permitir navegación por scroll suave.
- **Media Carousels:** Usa `.row.scroll` con tarjetas de ancho fijo (`small-width`) para permitir el desplazamiento horizontal de las portadas.
- **Interactive Cards:** Utiliza el patrón `.no-padding.round.wave` con efectos de hover que activan un panel de detalles (`.page.active`) con acciones rápidas (play, add, like).
- **Ranking System:** Etiquetas absolutas numéricas para destacar el orden de popularidad.

## Código Fuente
```html
<!-- Netflix Layout Structure -->
<div class="white-text dark-mode">
  <!-- Top Navigation -->
  <nav class="top top-shadow white-text">
    <img src="netflix-logo.png" alt="Netflix">
    <!-- Desktop Links -->
    <button class="small-round large transparent l">Home</button>
    <button class="small-round large transparent l">Series</button>
    <button class="small-round large transparent l">Movies</button>
    <div class="max"></div>
    <!-- Actions -->
    <button class="circle large transparent"><i>search</i></button>
    <button class="circle large transparent m l"><i>notifications</i></button>
  </nav>

  <main>
    <!-- Hero Section -->
    <section id="home" class="large-height">
      <video class="responsive" autoplay loop muted>
        <source src="hero-video.mp4" type="video/mp4">
      </video>
      <div class="absolute top bottom left middle-align small left-shadow">
        <div class="large-padding">
          <h1 class="bold">Title of Show</h1>
          <p>Description of the featured series or movie...</p>
          <nav>
            <button class="small-round large white black-text">
              <i>play_arrow</i><span>Watch</span>
            </button>
            <button class="small-round large border white-border white-text">
              <i>info</i><span>More Info</span>
            </button>
          </nav>
        </div>
      </div>
    </section>

    <!-- Content Carousels -->
    <div class="padding">
      <h2 class="h5 bold">Popular on Netflix</h2>
      <div class="row scroll">
        <!-- Media Card -->
        <div class="no-padding small-round small-width wave">
          <img class="responsive" src="poster.jpg">
          <!-- Details on Hover (Conceptual) -->
          <div class="page padding absolute left right bottom">
             <nav>
               <button class="circle border small white-text"><i>play_arrow</i></button>
               <button class="circle border small white-text"><i>add</i></button>
             </nav>
          </div>
        </div>
        <!-- Repeat cards... -->
      </div>

      <h2 class="h5 bold" id="series">Series</h2>
      <div class="row scroll">
        <!-- More cards... -->
      </div>
    </div>
  </main>
</div>
```
