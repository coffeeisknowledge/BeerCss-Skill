# Music Player Template

## Descripción
Este template recrea una interfaz de reproductor de música moderna y minimalista. Se caracteriza por un fondo de pantalla completa dinámico (`fixed.back`), controles de reproducción centrados, el uso de formas decorativas (`shape`) y carruseles de álbumes responsivos.

## Estructura Clave
- **Dynamic Background:** Un contenedor `.fixed.top.right.bottom.left.back` que muestra la carátula del álbum como fondo de pantalla completa.
- **Glassmorphism:** El contenedor principal del reproductor usa `.large-padding.small-blur.round` para un efecto de desenfoque sutil.
- **Player controls:**
  - **Album Art:** Usa una forma decorativa `.shape.sided-cookie6` con rotación (`rotate`).
  - **Progress Slider:** Implementa `.slider` con un `tooltip` para el indicador de tiempo.
  - **Playback Buttons:** Usa combinaciones de `.extra.circle` para el Play/Pause y `.fill.large` para Skip.
- **Album Grid (Desktop):** Un `.grid.large-space` que organiza las carátulas de otros álbumes en columnas.
- **Album Scroll (Mobile):** Usa `nav.scroll` para mostrar una lista horizontal de carátulas en pantallas pequeñas.

## Código Fuente
```html
<!-- Music Player Layout Structure -->
<div class="music-player-layout">
  <!-- Dynamic Fullscreen Background -->
  <div class="fixed top right bottom left back no-events">
    <img src="album-bg.jpg" class="responsive page active bottom">
  </div>

  <!-- Main Player Container -->
  <main class="middle-align center-align">
    <div class="large-padding small-blur round white-text">
      <div class="grid middle-align large-space">
        <!-- Left: Active Track Info -->
        <div class="s12 m6 l6">
          <div class="round no-padding">
            <!-- Rotating Album Art -->
            <div class="shape sided-cookie6 medium-width medium-height space rotate auto-margin">
              <img src="current-album.jpg" class="responsive">
            </div>
            <div class="center-align">
              <h6>Track Title</h6>
              <div>Artist Name</div>
            </div>
            <!-- Progress Bar -->
            <div class="large-padding">
              <div class="slider">
                <input type="range" value="50">
                <span></span>
                <span class="tooltip"></span>
              </div>
              <!-- Playback Controls -->
              <nav class="center-align">
                <button class="fill large"><i>skip_previous</i></button>
                <button class="extra circle large-padding"><i>play_arrow</i></button>
                <button class="fill large"><i>skip_next</i></button>
              </nav>
            </div>
          </div>
        </div>

        <!-- Right: Playlist / Other Albums -->
        <div class="s12 m6 l6 l">
          <div class="grid large-space">
            <div class="s12 m6">
              <a class="row round medium-height"><img src="album1.jpg" class="responsive"></a>
              <div class="space"></div>
              <a class="row round small-height"><img src="album2.jpg" class="responsive"></a>
            </div>
            <div class="s12 m6">
              <a class="row round small-height"><img src="album3.jpg" class="responsive"></a>
              <div class="space"></div>
              <a class="row round medium-height"><img src="album4.jpg" class="responsive"></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</div>
```
