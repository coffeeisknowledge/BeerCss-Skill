# YouTube Clone Template

## Descripción
Este template replica la experiencia de YouTube, enfocándose en una cuadrícula de videos responsiva, una barra lateral de navegación extensa y filtros de categoría superiores. Utiliza patrones de "video cards" con miniaturas y menús contextuales.

## Estructura Clave
- **Top App Bar:** Usa `nav.top.surface` para el logo, barra de búsqueda centrada y acciones de usuario (notificaciones, creación).
- **Left Sidebar (Navigation Rail/Drawer):** Usa `nav.left.m.l.scroll` con soporte para modo expandido (`max`). Contiene enlaces a Home, Tendencias, Suscripciones y Biblioteca.
- **Category Chips:** Usa `nav.group.connected.scroll.fill` en la parte superior del contenido para filtrar por categorías.
- **Main Content (Video Grid):** Usa `.grid` con celdas `.s12.m6.l3` para mostrar las miniaturas de video de forma responsiva.
- **Video Card Pattern:** Cada video es un contenedor `.round` con una imagen `.responsive`, una etiqueta de duración absoluta y un área de texto con título en negrita (`bold`) y vistas.
- **Horizontal Scrolls:** Usa `.row.scroll` para secciones como "What's hot" o "Your videos", permitiendo carruseles horizontales.

## Código Fuente
```html
<!-- YouTube Layout Structure -->
<div id="layout">
  <!-- Top Bar -->
  <nav class="top surface">
    <img src="youtube-logo.png" alt="YouTube">
    <div class="max"></div>
    <div class="max field round suffix prefix small no-margin m l white black-text">
      <i class="front">search</i>
      <input type="text" placeholder="Search">
      <i class="front">mic</i>
    </div>
    <div class="max"></div>
    <button class="circle large transparent s"><i>search</i></button>
    <button class="circle large transparent m l"><i>video_call</i></button>
    <button class="circle large transparent m l"><i>notifications</i></button>
  </nav>

  <!-- Left Navigation (Desktop) -->
  <nav class="left m l scroll">
    <header>
      <button class="circle extra transparent"><i>menu</i></button>
    </header>
    <a class="active"><i>home</i><span>Home</span></a>
    <a><i>whatshot</i><span>What's hot</span></a>
    <a><i>subscriptions</i><span>Subscriptions</span></a>
    <hr>
    <a><i>video_library</i><span>Library</span></a>
    <a><i>history</i><span>History</span></a>
  </nav>

  <!-- Main Content -->
  <main>
    <div class="page active">
      <!-- Category Filters -->
      <nav class="group connected scroll fill">
        <button class="left-round active"><span>All</span></button>
        <button class="no-round"><span>Music</span></button>
        <button class="no-round"><span>Gaming</span></button>
        <button class="right-round"><span>Live</span></button>
      </nav>

      <!-- Video Grid -->
      <div class="grid">
        <div class="s12 m6 l3">
          <div class="round">
            <div class="wave">
              <img class="responsive" src="thumbnail.jpg">
              <div class="absolute right top large-margin black white-text small-text">10:00</div>
            </div>
            <div class="padding">
              <nav>
                <div class="max truncate">
                  <div class="bold">Video Title goes here</div>
                  <div>1.2M views • 2 days ago</div>
                </div>
                <button class="circle transparent"><i>more_vert</i></button>
              </nav>
            </div>
          </div>
        </div>
        <!-- Repeat for more videos -->
      </div>

      <!-- Horizontal Section -->
      <h2 class="h5">What's hot</h2>
      <div class="row scroll">
        <div class="border small-width small-round">
          <!-- Small card content -->
        </div>
      </div>
    </div>
  </main>

  <!-- Bottom Nav (Mobile) -->
  <nav class="bottom s">
    <a class="active"><i>home</i><span>Home</span></a>
    <a><i>explore</i><span>Explore</span></a>
    <a class="button square round extra fill"><i>add</i></a>
    <a><i>subscriptions</i><span>Subscriptions</span></a>
  </nav>
</div>
```
