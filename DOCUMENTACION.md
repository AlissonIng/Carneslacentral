# Documentación del Proyecto: Carnes & Abarrotes La Central

## 1. Introducción y Sustentación del Proyecto
El presente documento tiene como objetivo sustentar técnica y visualmente el desarrollo del sitio web para **Carnes & Abarrotes La Central**. Este proyecto fue desarrollado utilizando un flujo de trabajo colaborativo profesional basado en Git y GitHub, dividiendo el trabajo en tres ramas (branches) principales para evitar conflictos y asegurar la escalabilidad del código.

A continuación, se detalla el paso a paso del flujo de control de versiones y la explicación técnica de cada componente desarrollado por los distintos equipos.

---

## 2. Equipo A: Catálogo de Productos
**Rama (Branch):** `feature/catalogo`

### Flujo de Git (Paso a paso)
Para integrar esta sección de manera segura al proyecto principal, el Equipo A ejecutó el siguiente flujo:
```bash
# 1. Crear y moverse a la rama específica del catálogo
git checkout -b feature/catalogo

# 2. Registrar los cambios realizados en index.html (sección catálogo) y la carpeta img/
git add .

# 3. Guardar el estado local con un mensaje claro y descriptivo
git commit -m "feat: integración de catálogo de productos con CSS Grid e imágenes locales"

# 4. Subir la rama al repositorio remoto en GitHub
git push origin feature/catalogo
```
*Tras subir la rama, se procede a crear un **Pull Request (PR)** en GitHub hacia la rama `main`.*

### Explicación del Código (`<section id="catalogo">`)
- **Estructura HTML (`.catalogo-grid`)**: Se implementó una cuadrícula (Grid) responsiva. Cada ítem (`.product-card`) actúa como una tarjeta que agrupa la imagen, el tipo de producto, su nombre, descripción y precio.
- **Implementación de Imágenes**: Se reemplazaron los *placeholders* (emojis temporales) por imágenes en alta resolución ubicadas en la ruta local `img/`. Las etiquetas `<img>` tienen la propiedad CSS `object-fit: cover` para mantener proporciones exactas sin distorsionarse.
- **Estilos CSS y Efectos**: 
  - Se configuró `grid-template-columns: repeat(auto-fill, minmax(260px, 1fr))` para que el catálogo se adapte automáticamente al tamaño de la pantalla (móvil, tablet o PC).
  - Al hacer hover (pasar el ratón por encima) sobre una tarjeta (`.product-card:hover`), el CSS aplica una sutil sombra (`box-shadow`) y eleva la tarjeta (`transform: translateY(-4px)`), generando interactividad moderna.

---

## 3. Equipo C: Galería e Imagen Corporativa
**Rama (Branch):** `feature/galeria`

### Flujo de Git (Paso a paso)
```bash
# 1. Moverse desde la rama principal a una nueva rama de galería
git checkout -b feature/galeria

# 2. Agregar los cambios del layout de galería
git add .

# 3. Guardar el progreso
git commit -m "feat: diseño de galería en mosaico y efectos hover"

# 4. Enviar al servidor de GitHub
git push origin feature/galeria
```

### Explicación del Código (`<section id="galeria">`)
- **Estructura HTML (`.galeria-grid`)**: Se construyó un layout estilo mosaico con contenedores `.galeria-item` que envuelven fondos visuales y un texto superpuesto (`.galeria-overlay`).
- **CSS Grid Avanzado**: Se utilizó `grid-template-columns: repeat(3, 1fr)` para dividir la sección en tres columnas iguales. El primer elemento de la galería (`.galeria-item:first-child`) tiene la instrucción `grid-row: span 2`, lo que significa que ocupa dos filas de alto, creando un efecto de diseño asimétrico y dinámico.
- **Efectos de Overlay y Transiciones**:
  - Originalmente, la capa de texto (`.galeria-overlay`) tiene `opacity: 0` (invisible).
  - Cuando el usuario pasa el cursor (`:hover`), la opacidad pasa a `1` revelando el texto con un degradado inferior, mientras la imagen interna se amplía ligeramente (`transform: scale(1.06)`) aportando un toque premium al sitio.

---

## 4. Equipo B: Página de Contacto
**Rama (Branch):** `feature/contacto`

### Flujo de Git (Paso a paso)
```bash
# 1. Moverse a la rama de contacto
git checkout -b feature/contacto

# 2. Preparar los archivos (CSS mejorado y HTML modificado)
git add .

# 3. Hacer el commit con detalles estéticos
git commit -m "feat: rediseño estético de contacto con glassmorphism y micro-animaciones"

# 4. Subir rama para el Pull Request
git push origin feature/contacto
```

### Explicación del Código (`<section id="contacto">`)
- **Estructura HTML**: Dividida en dos columnas mediante la clase `.contacto-layout`. A la izquierda, una lista de información (`.info-list`) con ubicación, horarios y teléfono. A la derecha, un formulario interactivo (`.contact-form`).
- **Diseño Estético Premium (Glassmorphism)**: 
  - El formulario emplea un diseño moderno y translúcido. Se utiliza `background: rgba(255, 255, 255, 0.03)` junto con `backdrop-filter: blur(10px)` para desenfocar el fondo y simular un panel de cristal esmerilado.
- **Micro-animaciones (Hover Effects)**:
  - **Íconos**: Poseen fondos con gradientes (`linear-gradient`) y una leve sombra. Al pasar el cursor, aumentan de escala y su sombra cambia al tono corporativo, dando sensación de un botón físico.
  - **Botón de Envío (`.btn-send`)**: Utiliza un gradiente lineal. Al pasar el cursor, no solo invierte ligeramente el gradiente, sino que se desplaza hacia arriba e intensifica su luz inferior, creando un estilo altamente interactivo.
- **Fondo de Sección**: Incorpora un falso destello radial (`radial-gradient`) en su pseudo-elemento `::before` para añadir iluminación direccional asimétrica.

---

## 5. Cambios Globales y Adicionales
Durante la fase de consolidación (Merge), se realizaron ajustes que afectan transversalmente el código:
- **Favicon y Nav-Logo**: En el `<head>`, se insertó `<link rel="icon" type="image/png" href="img/Logo La Central 2.png" />` para establecer el icono de pestaña. Este mismo logo se incrustó en la barra de navegación usando Flexbox para alinear perfectamente la imagen corporativa con el texto "La Central".
- **Hero Header**: El fondo de la sección `#inicio` se actualizó mediante el reemplazo de una URL externa (Unsplash) por una ruta local `url('img/Fondo Inicio.jpg')`, garantizando la autonomía del recurso. El "badge" de año de inicio adquirió visibilidad mejorada gracias a la técnica de glassmorphism con desenfoque adaptado al fondo.

## 6. Conclusión y Publicación
Una vez unidas las ramas `feature/catalogo`, `feature/galeria` y `feature/contacto` mediante los respectivos **Pull Requests**, el código final reside en la rama `main`.
La validación semántica (HTML) y la optimización en hojas de estilo (CSS vanilla) aseguran tiempos de carga óptimos y una visualización responsiva impecable en dispositivos móviles y de escritorio.

El paso final será activar **GitHub Pages** desde la configuración del repositorio, de manera que GitHub procesará este `index.html` y los recursos de `img/` para exponerlos en un entorno de producción público.
