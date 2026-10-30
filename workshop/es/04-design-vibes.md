<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización desde el diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Este enfoque empieza por el diseño: define la visión, perfecciona el aspecto y deja que Copilot se encargue del trabajo pesado con CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Introduce este prompt:

> Quiero transformar esta página en una experiencia completa de arcade retro. Planifica una renovación visual integral que incluya: efectos de líneas de barrido CRT en el fondo, un brillo de neón pulsante en el título, una insignia VS animada con cambios de color en el degradado, una capa de brillo y destellos en las tarjetas de resultados de usuarios, animaciones de entrada flotante en los campos, texto de carga que alterne entre verde y morado, y efectos de resplandor al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) y los colores de acento verde (`#5fed83`) y morado (`#8a2be2`). Usa un tema oscuro con la fuente retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado que cubra todos los efectos visuales. **No lo aceptes de inmediato**: revísalo e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo: «Haz que el pulso de neón sea más lento, de unos 3 segundos»).
- Pregunta por efectos concretos (por ejemplo: «¿Cómo funcionará la capa de destellos en las tarjetas?»).
- Pide cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés satisfecho con el plan, pide a Copilot que lo implemente.

> Implementa el plan del tema retro arcade que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a las hojas de estilo. Esto puede incluir:

- `@keyframes` para líneas de barrido, pulsos de neón, destellos y efectos de entrada flotante.
- Pseudoelementos (`::before`, `::after`) para efectos superpuestos.
- Propiedades personalizadas de CSS para los colores del tema.
- Transiciones y estados al pasar el cursor por encima de elementos interactivos.

<!-- track:cli:start -->
Cuando se apliquen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta el estilo

> **⚠️ ¿No ves los cambios?** Si el nuevo tema o las animaciones no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y fuerza la recarga (`Ctrl+Shift+R`) en el navegador.

Mantén abierta la vista previa del navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un parpadeo eléctrico sutil al texto del título.

> La insignia VS debería pulsar de forma más marcada.

Este es un **proceso de desarrollo desde el diseño**: iteras sobre el resultado visual en tiempo real. Cada prompt perfecciona la experiencia. No te conformes con algo «suficientemente bueno»: ajusta el estilo hasta que la página parezca una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Las instrucciones deben reflejar las decisiones de diseño importantes para que los prompts posteriores mantengan la coherencia.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Añade a `copilot-instructions.md` una sección de guía de diseño que describa el tema de arcade retro: colores, fuentes y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Actualiza las instrucciones del repositorio con una guía breve del tema de arcade retro: colores, fuentes, estilo de animación y la regla de que las nuevas interfaces deben conservar la estética de neón.
<!-- track:cli:end -->

Cuando la página y el diseño estén listos, haz commit de las instrucciones y los cambios de diseño.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para **diseñar un sistema visual antes de implementarlo**.
- **Iterar sobre el resultado visual** con comentarios breves.
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener la identidad visual.
