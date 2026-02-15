# Reddit Clone Template

## Descripción
Este template recrea la interfaz de Reddit, enfocándose en un feed de publicaciones con sistema de votación lateral, una barra de navegación superior fija con búsqueda global y selectores de comunidad, y una barra lateral derecha para información contextual y posts recientes.

## Estructura Clave
- **Fixed Header:** Usa `header.fixed.surface` para la navegación superior. Incluye selectores de comunidad (`.field.round.suffix.prefix`) y búsqueda.
- **Top Navigation Items:** Botones circulares transparentes con tooltips (`.tooltip.bottom`) para acciones como Chat, Notificaciones y Crear Post.
- **Feed de Publicaciones:** Usa un `.grid` donde la columna principal (`.s12.m12.l8`) contiene los posts y la secundaria (`.l4`) el sidebar.
- **Post Card Pattern:** Estructura de `.row.top-align`. Contiene un panel de votación vertical (`nav.vertical.no-space`) y un área de contenido con metadatos del autor y contenido multimedia (imágenes o links).
- **Sub-navigation:** Chips (`button.chip`) con scroll horizontal para filtrar el feed (Best, Hot, New).
- **Sidebar:** Compuesto por elementos `article.no-elevate.round` para secciones de Premium, Home info y Recent Posts.
- **Create Post Dialog:** Un `dialog` complejo con pestañas (`.tabs.scroll`) para diferentes tipos de contenido (Post, Media, Link).

## Código Fuente
```html
<!-- Reddit Layout Structure -->
<div class="layout">
  <!-- Top Navigation Bar -->
  <header class="fixed surface">
    <nav>
      <img src="reddit-logo.svg" style="width: 100px">
      <!-- Community Selector -->
      <div class="max l">
        <div class="field fill round prefix suffix">
          <i>home</i>
          <input value="Home" readonly>
          <i>arrow_drop_down</i>
          <menu>
            <li>r/beercss</li>
            <li>r/materialdesign</li>
          </menu>
        </div>
      </div>
      <!-- Global Search -->
      <div class="max">
        <div class="field fill round prefix">
          <i>search</i>
          <input placeholder="Search">
        </div>
      </div>
      <!-- Action Icons -->
      <button class="transparent circle l"><i>trending_up</i><span class="tooltip bottom">Popular</span></button>
      <button class="transparent circle l m"><i>notifications</i></button>
      <!-- Profile Button -->
      <button class="transparent small-round small-padding">
        <img src="avatar.png" class="responsive">
        <span class="vertical small-text left-align">
          <span>username</span>
          <span>999 karma</span>
        </span>
        <i>arrow_drop_down</i>
      </button>
    </nav>
  </header>

  <main class="responsive">
    <div class="grid">
      <!-- Main Feed -->
      <div class="s12 m12 l8">
        <!-- Create Post Entry -->
        <div class="row">
          <img src="avatar.png" class="circle small">
          <div class="max field fill round"><input placeholder="Create Post"></div>
          <button class="transparent circle"><i>image</i></button>
        </div>

        <!-- Post Row -->
        <div class="row top-align">
          <!-- Voting Panel -->
          <nav class="vertical no-space grey-text top-align">
            <button class="transparent circle"><i>thumb_up</i></button>
            <div>Vote</div>
            <button class="transparent circle"><i>thumb_down</i></button>
          </nav>
          <!-- Post Content -->
          <div class="max">
            <div class="row">
              <img src="community-icon.png" class="circle small">
              <div class="max">
                <b>r/sveltejs</b> • <label class="grey-text">Posted by u/user 3h ago</label>
                <h6 class="no-margin">Post Title Headline</h6>
              </div>
            </div>
            <p>Post body content goes here...</p>
            <nav>
              <button class="transparent"><i>chat_bubble</i><span>15 Comments</span></button>
              <button class="transparent"><i>share</i><span>Share</span></button>
            </nav>
          </div>
        </div>
        <hr class="large">
      </div>

      <!-- Right Sidebar -->
      <div class="s12 m12 l4">
        <article class="no-elevate round">
          <h6>About Community</h6>
          <p>Community description text...</p>
          <nav class="vertical">
            <button class="responsive">Create Post</button>
            <button class="responsive border">Join</button>
          </nav>
        </article>
      </div>
    </div>
  </main>
</div>
```
