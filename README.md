# El Pradon de Santa Marina

Sitio web estatico de los apartamentos rurales El Pradon de Santa Marina, en Parres, Llanes, Asturias.

## Arquitectura

El proyecto utiliza una arquitectura deliberadamente pequena y sin proceso de compilacion:

```text
.
|- .github/
|  `- copilot-instructions.md
|- El-Pradon-Atelier-Bosque.html
|- LICENSE
`- README.md
```

- `El-Pradon-Atelier-Bosque.html` es el punto de entrada y contiene la estructura HTML, los estilos CSS y la logica JavaScript de la experiencia.
- `.github/copilot-instructions.md` contiene el contexto y las reglas que debe seguir GitHub Copilot en este proyecto.
- `LICENSE` aplica al codigo y la documentacion del proyecto.
- No hay framework, gestor de dependencias ni paso de build.

La pagina carga algunos recursos externos en tiempo de ejecucion:

- Fotografias desde `www.elpradondesantamarina.es`.
- Tipografias desde Google Fonts.
- Enlaces externos a Google Maps y al telefono/correo de contacto.

Por ese motivo, el HTML funciona mejor con conexion a Internet. Si una fotografia remota no esta disponible, la interfaz muestra un estado alternativo.

## Puesta en marcha

Para una comprobacion rapida, abre [El-Pradon-Atelier-Bosque.html](El-Pradon-Atelier-Bosque.html) directamente en un navegador.

Para servirlo desde un servidor local en Windows:

```powershell
python -m http.server 8000
```

Despues visita `http://localhost:8000/El-Pradon-Atelier-Bosque.html`.

## Desarrollo

Al trabajar en la pagina:

1. Conserva la estructura de una sola pagina salvo que exista una necesidad real de separar recursos.
2. Mantiene la experiencia responsive para escritorio, tablet y movil.
3. Comprueba los flujos de navegacion, cambio de idioma, galeria, dialogo de consulta y enlaces de contacto despues de modificar JavaScript.
4. Verifica el estado sin conexion de las imagenes y el comportamiento con `prefers-reduced-motion` cuando toques la presentacion.
5. No sustituyas fotografias, textos de negocio o datos de contacto sin una indicacion expresa.

## Publicacion

El proyecto puede publicarse en cualquier alojamiento de archivos estaticos. Copia el HTML y sirve el archivo como pagina de entrada. No se necesita un servidor de aplicaciones.

## Licencia

El codigo y la documentacion se distribuyen bajo la licencia MIT. Las fotografias, marcas, textos y recursos remotos de terceros pueden estar sujetos a derechos o condiciones distintas; consulta `LICENSE` y las condiciones de sus respectivos propietarios.
