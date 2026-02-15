# Material Design 3 Template

## Descripción
Este template actúa como un "showcase" exhaustivo de Material Design 3 utilizando BeerCSS. Presenta una disposición de portal de documentación con un sidebar de navegación izquierdo, secciones de contenido responsivas que destacan componentes específicos (toolbars, cards, progress indicators) y un pie de página detallado con enlaces institucionales.

## Estructura Clave
- **Navigation Rail (Left):** `nav.left.l` con soporte para expansión (`max`). Contiene iconos SVG personalizados para secciones como Home, Develop, Foundations y Styles.
- **Top App Bar (Mobile):** `nav.top.s.m` para navegación compacta en pantallas pequeñas.
- **Hero Section:** Un `.grid` inicial con un mensaje de bienvenida en un lado (`article.no-elevate.round`) y un video demostrativo en el otro.
- **Responsive Sections:** Uso intensivo de `section.responsive` para agrupar tarjetas de componentes y artículos de blog.
- **Component Showcase Grid:** Cuadrículas `.grid` con celdas `.s12.m6.l4` para mostrar ejemplos de "Expressive Components".
- **Interaction Pattern:** Uso de `.wave` y `.page` para animaciones de transición y efectos de clic en las tarjetas de recursos populares.
- **Institutional Footer:** Un área compleja con `hr`, cuadrículas de enlaces organizadas por categorías (Social, Libraries, Archived) y logos oficiales.

## Código Fuente
```html
<!-- Material Design 3 Layout Structure -->
<div class="m3-layout">
  <!-- Left Navigation Rail -->
  <nav class="left l">
    <header>
      <button class="circle extra transparent"><i>menu</i></button>
    </header>
    <a class="active"><i>home</i><span>Home</span></a>
    <a><i>apps</i><span>Get started</span></a>
    <a><i>code</i><span>Develop</span></a>
    <a><i>palette</i><span>Styles</span></a>
    <div class="max"></div>
    <button class="border circle"><i>dark_mode</i></button>
  </nav>

  <main>
    <!-- Hero Banner -->
    <div class="grid">
      <div class="s12 m6 l6">
        <article class="no-elevate round large-height large-padding middle-align">
          <div class="large-padding">
            <h1 class="large">Material Design</h1>
            <h2 class="h6">Build beautiful, usable products with MD3.</h2>
            <nav><button class="extra">Get started</button></nav>
          </div>
        </article>
      </div>
      <div class="s12 m6 l6">
        <div class="round large-height no-padding">
          <video class="responsive" autoplay loop muted><source src="hero.mp4"></video>
        </div>
      </div>
    </div>

    <!-- Expressive Components Section -->
    <section class="responsive">
      <h2>Expressive components</h2>
      <div class="grid">
        <div class="s12 m6 l6">
          <article class="round no-elevate no-padding wave">
            <img src="toolbars.png" class="responsive large">
            <div class="large-padding">
              <h3>New: Toolbars</h3>
              <p>Flexible component to display frequently used actions.</p>
            </div>
          </article>
        </div>
        <!-- More component cards... -->
      </div>
    </section>

    <!-- Resources Footer -->
    <section class="responsive">
      <hr>
      <div class="grid">
        <div class="s12 l6">
          <p>Material Design is an adaptable system of guidelines...</p>
        </div>
        <div class="s12 l6">
          <div class="grid large-line">
            <div class="s4">
              <p class="bold">Libraries</p>
              <p><a class="link">Android</a></p>
              <p><a class="link">Web</a></p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</div>
```
