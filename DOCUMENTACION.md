# Documentación del Proyecto: Carnes & Abarrotes La Central

## Información General
- **Asignación:** Equipo A
- **Sección a cargo:** Catálogo de Productos
- **Rama (Branch):** `feature/catalogo`
- **Descripción:** Taller Práctico de GitHub para desarrollo web de empresa de cárnicos y abarrotes.

## Cambios Realizados en el Código
Se realizaron las siguientes modificaciones en el archivo `index.html` dentro de la sección de **Catálogo de productos** (`<section id="catalogo">`):

1. **Reemplazo de Placeholders por Imágenes Reales:**
   - Se eliminaron los elementos `div` con clase `product-img-placeholder` que contenían emojis.
   - Se implementaron etiquetas `<img>` con clase `product-img` en cada uno de los 6 productos.
   - Las imágenes fueron enlazadas a los archivos proporcionados en la carpeta local `img/` (ej. `img/Lomo de res.jpg`, `img/Costilla de cerdo.webp`, etc.).
   - Estos cambios mejoran la estética visual y brindan una experiencia más inmersiva al usuario.

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
git commit -m "feat: mejora visual del catálogo con imágenes locales"

# 4. Subir la rama al repositorio remoto
git push origin feature/catalogo
```

> **Siguiente paso en GitHub:**
> Ingresar a `github.com` en el repositorio del proyecto, dar clic en **'Compare & pull request'**, describir los cambios y solicitar revisión al compañero de equipo asignado.
