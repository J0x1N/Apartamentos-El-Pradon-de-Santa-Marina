# Instrucciones del proyecto para GitHub Copilot

## Contexto

Este repositorio contiene la web estatica de los apartamentos rurales El Pradon de Santa Marina, en Parres, Llanes, Asturias. El punto de entrada es `El-Pradon-Atelier-Bosque.html`.

La pagina es una single-page autocontenida: HTML, CSS y JavaScript viven en el mismo archivo. Usa imagenes remotas del dominio del alojamiento, Google Fonts y enlaces externos de contacto y mapas. No hay framework, package manager ni proceso de compilacion.

## Reglas de trabajo

- Lee el HTML existente antes de editarlo y localiza el bloque que controla el comportamiento solicitado.
- Mantiene la arquitectura estatica y sin dependencias nuevas salvo que el usuario pida expresamente una migracion.
- Conserva el idioma espanol, la version inglesa, el contenido del alojamiento y los datos de contacto salvo indicacion expresa.
- Preserva la accesibilidad: HTML semantico, textos alternativos, foco visible, navegacion por teclado, estados `aria` y soporte para `prefers-reduced-motion`.
- Preserva el comportamiento responsive en escritorio, tablet y movil.
- No reemplaces fotografias, tipografias, URLs o textos comerciales por contenido inventado.
- Evita refactorizaciones amplias o cambios de formato no relacionados con la tarea.
- Usa nombres descriptivos y conserva el estilo compacto del archivo existente cuando sea posible.
- No anadas librerias, configuracion de build o carpetas de recursos si la tarea no las necesita.
- Documenta en `README.md` cualquier cambio que altere la arquitectura, la forma de ejecucion o las dependencias externas.

## Validacion

Despues de editar:

1. Comprueba que el HTML sigue siendo valido y que no quedan etiquetas o bloques de script incompletos.
2. Abre la pagina en un navegador y revisa la navegacion, los dialogos, la galeria, el cambio de idioma y el formulario de consulta si el cambio afecta a esas areas.
3. Comprueba al menos un viewport movil y uno de escritorio cuando cambies CSS o layout.
4. Verifica que los recursos remotos fallan de forma tolerable y que los enlaces de contacto conservan sus destinos.
5. Revisa el diff y confirma que no se han modificado archivos ajenos a la tarea.

## Alcance de los cambios

Los cambios habituales deben limitarse a:

- `El-Pradon-Atelier-Bosque.html` para la experiencia web.
- `README.md` para documentacion publica.
- `.github/copilot-instructions.md` para el contexto de los agentes.
- `LICENSE` para los terminos de distribucion.

Si se necesita separar CSS, JavaScript o imagenes, explica primero el motivo en `README.md` y conserva el HTML como punto de entrada claro.
