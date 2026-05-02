# Documentación del Proyecto: Carnes & Abarrotes La Central

## Información General
- **Asignación:** Equipo A
- **Sección a cargo:** Catálogo de Productos
- **Rama (Branch):** `feature/catalogo`
- **Descripción:** Taller Práctico de GitHub para desarrollo web de empresa de cárnicos y abarrotes.

## Cambios Realizados en el Código
Se realizaron las siguientes modificaciones en el archivo `index.html`:

### 1. Sección Catálogo de Productos (`<section id="catalogo">`)
- **Reemplazo de Placeholders por Imágenes Reales:**
  - Se eliminaron los elementos `div` con clase `product-img-placeholder` que contenían emojis.
  - Se implementaron etiquetas `<img>` con clase `product-img` en cada uno de los 6 productos.
  - Las imágenes fueron enlazadas a los archivos proporcionados en la carpeta local `img/` (ej. `img/Lomo de res.jpg`, `img/Costilla de cerdo.webp`, etc.).

### 2. Sección de Contacto (`<section id="contacto">`)
- **Diseño Moderno y Glassmorphism:**
  - Se agregó un fondo semitransparente con desenfoque (`backdrop-filter: blur`) al formulario para crear un efecto glassmorphism.
  - Se implementó un gradiente oscuro con un brillo radial de fondo para mayor profundidad visual.
- **Micro-animaciones (Hover Effects):**
  - Los íconos de información ahora cuentan con gradientes fluidos y un efecto de escalado al pasar el cursor (`hover`), junto con sombras dinámicas.
  - El botón de envío fue mejorado con un gradiente dorado y una sutil animación de elevación y sombreado al interactuar con él, incrementando la estética premium del sitio.

## Validación y Estructura
La validación visual del código demuestra que la página mantiene su estructura semántica correcta y los estilos CSS base continúan aplicándose de manera impecable a los nuevos elementos (Responsive Grid, Hover effects y Box Shadows).

## Proceso de Git (Flujo Colaborativo)
De acuerdo a las instrucciones del taller, los siguientes comandos deben ejecutarse en la terminal para registrar y subir los cambios al repositorio central:

```bash
# 1. Asegurar estar en la rama correcta
git checkout -b feature/catalogo

# 2. Agregar los cambios del archivo index.html y la documentación
git add .

# 3. Guardar el estado con un commit descriptivo
git commit -m "feat: integración de imágenes locales y rediseño estético de la sección contacto"

# 4. Subir la rama al repositorio remoto
git push origin feature/catalogo
```

> **Siguiente paso en GitHub:**
> Ingresar a `github.com` en el repositorio del proyecto, dar clic en **'Compare & pull request'**, describir los cambios y solicitar revisión al compañero de equipo asignado.
