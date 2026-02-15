# Uber Clone Template

## Descripción
Este template simula la aplicación de Uber, utilizando un fondo de mapa a pantalla completa (`fixed`) y un panel de reserva prominente que cambia de posición según el dispositivo (sidebar izquierdo en desktop, drawer inferior en móvil).

## Estructura Clave
- **Full-Screen Map:** Usa un contenedor `.fixed.top.left.right.bottom` con una imagen `.responsive` para simular el mapa de fondo.
- **Top Navigation Bar:** `nav.top.black.white-text` para branding y menús de servicios (Ride, Drive).
- **Booking Card (Desktop):** Un `article.no-padding.medium-width.m.l.page.left` posicionado a la izquierda con elevación media.
- **Booking Drawer (Mobile):** Un `dialog.bottom.active.s` que actúa como el panel de interacción principal en pantallas pequeñas.
- **Form Patterns:** Secciones de color sólido (`black.white-text`) para el estado de la reserva y áreas blancas (`large-padding`) para inputs de búsqueda (`.field.prefix.round`) y listas de ubicaciones frecuentes.
- **Map Controls:** Botones flotantes circulares (`.fixed.bottom.right`) para zoom (+/-).

## Código Fuente
```html
<!-- Uber Layout Structure -->
<div class="uber-layout">
  <!-- Map Background -->
  <div class="fixed top left right bottom">
    <img src="map-background.jpg" class="responsive">
  </div>

  <!-- Top Navigation -->
  <nav class="top black white-text">
    <img src="uber-logo.png" height="24">
    <button class="large transparent m l">Ride</button>
    <button class="large transparent m l">Drive</button>
    <div class="max"></div>
    <button class="circle large transparent"><i>palette</i></button>
  </nav>

  <!-- Desktop Booking Sidebar -->
  <article class="no-padding large-margin medium-width m l absolute left top medium-elevate white">
    <!-- Header/State -->
    <div class="large-padding black white-text">
      <h5 class="bold">Where are you going?</h5>
      <nav class="right-align">
        <button class="transparent large white-text">Cancel</button>
      </nav>
    </div>
    <!-- Search / Favorites -->
    <div class="large-padding">
      <div class="field prefix round white black-text">
        <i>search</i>
        <input placeholder="Enter destination">
      </div>
      <ul class="list">
        <li>
          <button class="circle small no-wave"><i>gps_fixed</i></button>
          <div class="max">
            <h6 class="no-margin">Current Location</h6>
            <div class="link">123 Street Name</div>
          </div>
        </li>
      </ul>
    </div>
  </article>

  <!-- Mobile Booking Drawer -->
  <dialog class="bottom active s no-padding white">
    <div class="padding black white-text">
      <h5 class="bold">Where to?</h5>
    </div>
    <div class="large-padding">
      <div class="field prefix round white black-text">
        <i>search</i>
        <input placeholder="Enter destination">
      </div>
    </div>
  </dialog>

  <!-- Map Zoom Controls -->
  <div class="fixed bottom right margin m l">
    <button class="circle white black-text wave"><i>add</i></button>
    <div class="space"></div>
    <button class="circle white black-text wave"><i>remove</i></button>
  </div>
</div>
```
