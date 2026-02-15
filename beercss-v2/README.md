# BeerCSS v2 Super Skill (Local-Context Edition)

## 🌟 Visión General (Overview)

Bienvenido a la **BeerCSS v2 Super Skill**, una Agent Skill de alto rendimiento diseñada específicamente para **Gemini CLI**. Su propósito fundamental es permitir la generación de interfaces de usuario modernas, accesibles y 100% válidas bajo el framework BeerCSS y los principios de Material Design 3.

A diferencia de las implementaciones estándar, esta versión elimina las alucinaciones mediante el uso estricto de **contexto local**. Cada componente, clase y token de color se valida contra una biblioteca de documentación modularizada que actúa como la única fuente de verdad.

---

## 🏗️ Arquitectura del Sistema

La skill está organizada de forma modular para garantizar eficiencia y precisión en la recuperación de información (RAG):

- **`/rules` (Las Leyes Inmutables):** Contiene los protocolos críticos de comportamiento.
  - `no-hallucination.md`: Prohíbe el uso de clases inexistentes.
  - `color-system.md`: Define los design tokens oficiales (MD3) y variables CSS.
  - `decision-protocol.md`: Establece el flujo de interacción (proceder, verificar o preguntar).
- **`/components` (Biblioteca de Componentes):** Documentación migrada y optimizada de más de 35 componentes oficiales (Buttons, Cards, Grid, Inputs, etc.).
- **`/helpers` (Utilidades Modulares):** Guías rápidas para el sistema de diseño (Spacing, Sizing, Elevation, Responsive, Positioning).
- **`/templates` (Patrones de Diseño):** Ejemplos reales de arquitecturas complejas (Gmail, YouTube, Netflix, Uber, Reddit) para replicar disposiciones de UI probadas.
- **`SKILL.md` (El Cerebro/Orquestador):** Punto de entrada principal que carga dinámicamente las reglas y sirve como mapa de navegación para el agente.

---

## 🚀 Guía de Uso (How to Prompt)

### Activación
La skill se activa automáticamente al trabajar en el directorio del proyecto o al mencionar componentes de BeerCSS.

### Confianza Total en el Código
Puedes estar seguro de que los colores y clases generados son reales. El agente siempre consulta `rules/color-system.md` para asegurar que el tema (Light/Dark mode) se mantenga consistente sin usar hex codes "quemados".

### Ejemplos de Prompts
- **Básico:** *"Crea un botón primario usando el helper de elevación media."*
- **Estructura:** *"Genera un grid de 3 columnas que se apilen en móvil, con tarjetas bordeadas en cada celda."*
- **Complejo:** *"Necesito un formulario de login estilo Material Design 3 con validación de campo inválido."*
- **Plantillas:** *"Implementa un layout de lista de correos similar al de Gmail Clone."*

---

## 🔧 Mantenimiento

Esta Super Skill ha sido construida para ser escalable:

1. **Actualización de Componentes:** Si BeerCSS lanza una nueva versión, simplemente actualiza el archivo correspondiente en `components/` basándote en la documentación oficial.
2. **Nuevos Patrones:** Puedes añadir nuevos archivos en `templates/` siguiendo el estándar Markdown establecido para expandir las capacidades de diseño de la skill.
3. **Ajuste de Tokens:** Si tu proyecto cambia de marca, actualiza los valores en `rules/color-system.md` para que el agente adopte instantáneamente los nuevos colores corporativos.

---

**Proyecto:** BeerCSS Super Skill v2.0  
**Estado:** FINALIZADO ✅  
**Fecha:** 2026-02-15  
**Maintainer:** Claude
