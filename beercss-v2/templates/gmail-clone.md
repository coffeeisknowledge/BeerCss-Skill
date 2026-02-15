# Gmail Clone Template

## Descripción
Este template recrea la interfaz de Gmail utilizando una disposición de múltiples paneles (sidebars izquierdo y derecho) y un área central de contenido reactiva. Implementa patrones de navegación responsiva (bottom nav para móvil, rails para desktop) y controles de lista densos.

## Estructura Clave
- **Top App Bar:** Usa `nav.top.surface` para la búsqueda global y acciones de cuenta.
- **Left Sidebar (Navigation Rail):** Usa `nav.left.m.l` con soporte para expansión (`max`). Incluye el botón "Compose" prominentemente.
- **Right Sidebar (App Shortcut):** Usa `nav.right.m.l` para accesos rápidos a utilidades como Calendario o Contactos.
- **Bottom Navigation (Mobile):** Usa `nav.bottom.s` para la navegación principal en pantallas pequeñas.
- **Main Content:** Área `main.surface-container.round` que contiene la lista de correos y diálogos de composición.
- **Email List Pattern:** Filas construidas con `.row`, incluyendo checkboxes, botones de favoritos (`star`) y truncamiento de texto (`truncate`).

## Código Fuente
```html
<!-- Gmail Layout Structure -->
<div class="layout">
  <!-- Top Search Bar -->
  <nav class="top surface">
    <div class="max"></div>
    <div class="field round suffix prefix small no-margin m l white black-text">
      <i class="front">search</i>
      <input type="text" placeholder="Search mail">
      <i class="front">mic</i>
    </div>
    <div class="max"></div>
    <button class="circle large transparent s"><i>search</i></button>
    <button class="circle large transparent m l"><i>settings</i></button>
    <button class="circle large transparent m l"><i>apps</i></button>
  </nav>

  <!-- Left Navigation Rail (Desktop) -->
  <nav class="left m l">
    <header>
      <button class="circle extra transparent"><i>menu</i></button>
      <button class="primary-container square round extend">
        <i>edit</i>
        <span>Compose</span>
      </button>
    </header>
    <a class="active"><i>inbox</i><span>Inbox</span></a>
    <a><i>watch_later</i><span>Snoozed</span></a>
    <a><i>send</i><span>Sent</span></a>
    <a><i>insert_drive_file</i><span>Drafts</span></a>
  </nav>

  <!-- Bottom Nav (Mobile) -->
  <nav class="bottom s">
    <a class="active"><i>inbox</i><span>Inbox</span></a>
    <a><i>send</i><span>Sent</span></a>
    <a class="button fill square round extra"><i>edit</i></a>
    <a><i>insert_drive_file</i><span>Drafts</span></a>
  </nav>

  <!-- Main Inbox Content -->
  <main class="surface-container round padding">
    <!-- Toolbar -->
    <div class="row m l">
      <label class="checkbox"><input type="checkbox"><span></span></label>
      <button class="circle transparent"><i>refresh</i></button>
      <button class="circle transparent"><i>more_vert</i></button>
      <div class="max"></div>
      <label>1-50 of 100</label>
      <button class="circle transparent"><i>arrow_back</i></button>
      <button class="circle transparent"><i>arrow_forward</i></button>
    </div>

    <!-- Email Row Pattern -->
    <div class="row">
      <label class="checkbox m l"><input type="checkbox"><span></span></label>
      <button class="circle transparent m l"><i>star_outline</i></button>
      <button class="small circle s">A</button>
      <a class="max truncate left-align">
        <b>Sender Name - </b>
        <b>Subject Line - </b>
        <span>Preview of the email content that will be truncated...</span>
      </a>
      <label>12:03 PM</label>
    </div>
    <hr class="m l">
    <hr class="small s">
  </main>

  <!-- Right Utilities Rail -->
  <nav class="right m l center-align">
    <button class="circle transparent large">
      <img src="calendar-icon.png">
      <span class="tooltip left">Calendar</span>
    </button>
    <button class="circle transparent large">
      <img src="tasks-icon.png">
      <span class="tooltip left">Tasks</span>
    </button>
  </nav>
</div>
```
