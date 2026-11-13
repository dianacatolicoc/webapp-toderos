# WebApp Toderos Facatativá - Maquetación HTML5 y CSS3

Proyecto formativo del programa **Tecnólogo en Análisis y Desarrollo de Software (ADSO)** del **SENA**.

## 1. Descripción del Proyecto

**Título del proyecto:** *Desarrollo de WebApp para contratación segura de servicios domésticos y técnicos en Facatativá.*

Esta aplicación web busca conectar de forma confiable a personas que requieren servicios domésticos y técnicos en el municipio de Facatativá con prestadores independientes de oficios varios ("toderos").

La plataforma contempla tres roles de usuario:
* **Cliente:** Busca servicios, consulta perfiles, solicita visitas técnicas y califica la atención.
* **Prestador (Todero):** Publica sus oficios, define tarifas base, gestiona solicitudes y actualiza sus estados.
* **Administrador:** Supervisa usuarios, solicitudes, servicios activos y monitorea métricas de la plataforma.

---

## 2. Tecnologías y Restricciones Técnicas

La entrega se realizó cumpliendo estrictamente los lineamientos formativos de una primera maquetación estructural y visual:

* **HTML5 semántico:** Uso exclusivo de etiquetas estructuradas (`<main>`, `<header>`, `<nav>`, `<section>`, `<article>`, `<form>`, `<fieldset>`, `<table>`, `<footer>`).
* **CSS3 puro:** Sin preprocesadores ni dependencias externas. Estilos organizados entre un archivo global (`styles.css`) y archivos individuales por pantalla.
* **Sin JavaScript:** Toda la interactividad visual se basa en navegación de enlaces y controles nativos de formulario.
* **Sin librerías ni frameworks:** 0% uso de Bootstrap, Tailwind, React u otros.
* **Sin imágenes externas, fotos, íconos externos, SVG ni emojis:** Todos los elementos gráficos (avatares, espacios de mapas, gráficos de barras y logotipos) están representados mediante bloques neutros y cajas construidas únicamente con CSS.

---

## 3. Estructura del Proyecto

```text
webApp-toderos/
│
├── index.html              # Pantalla 1: Inicio de sesión
├── registro.html           # Pantalla 2: Registro de cuenta (Cliente / Todero)
├── buscar-servicios.html   # Pantalla 3: Catálogo y búsqueda de servicios (Cliente)
├── solicitar-servicio.html # Pantalla 4: Formulario para solicitar servicio
├── mis-servicios.html      # Pantalla 5: Panel del prestador (Mis servicios)
├── admin-dashboard.html    # Pantalla 6: Dashboard y métricas generales (Admin)
├── admin-usuarios.html     # Pantalla 7: Tabla de gestión y filtros de usuarios (Admin)
│
├── css/
│   ├── styles.css            # Estilos globales compartidos (variables, reset, layout base)
│   ├── index.css             # Estilos específicos de Inicio de sesión
│   ├── registro.css          # Estilos específicos de Registro
│   ├── buscar-servicios.css  # Estilos específicos de Búsqueda de servicios
│   ├── solicitar-servicio.css# Estilos específicos de Solicitud de servicio
│   ├── mis-servicios.css     # Estilos específicos de Mis servicios (Prestador)
│   ├── admin-dashboard.css   # Estilos específicos del Dashboard Administrativo
│   └── admin-usuarios.css    # Estilos específicos de Gestión de usuarios
│
└── README.md               # Documentación general del proyecto
```

---

## 4. Pantallas Desarrolladas

1. **Inicio de sesión (`index.html`)**:
   * Encabezado institucional con logotipo básico `TF` y título.
   * Campos de correo electrónico y contraseña.
   * Botón de inicio de sesión y botón alternativo en bloque neutro.
   * Enlaces directos a recuperación de contraseña, registro y acceso al panel administrativo.

2. **Registro (`registro.html`)**:
   * Selector accesible de tipo de cuenta (*Cliente* o *Todero*).
   * Formulario con nombre completo, celular, municipio fijado en Facatativá, correo y confirmación de contraseña.
   * Casilla de aceptación de términos y políticas.
   * Enlace para volver al inicio de sesión.

3. **Buscar servicios (`buscar-servicios.html`)**:
   * Barra de búsqueda por oficio o necesidad.
   * Filtros rápidos en etiquetas (Plomería, Electricidad, Pintura, Carpintería, Aseo).
   * Espacio representativo del mapa local en Facatativá (bloque neutro con texto descriptivo).
   * Tarjetas de prestadores destacados con foto simulada `[Foto]`, nombre, oficio, sector, calificación textual, tarifa y botón para solicitar.

4. **Solicitar servicio (`solicitar-servicio.html`)**:
   * Resumen del prestador seleccionado con datos clave de contacto y tarifa.
   * Formulario para seleccionar categoría de trabajo, descripción detallada, fecha, hora estimada, dirección y barrio de Facatativá.
   * Botones de envío y cancelación.

5. **Mis servicios (`mis-servicios.html`)**:
   * Barra superior con perfil del todero y calificación promedio.
   * Cajas de métricas rápidas (servicios activos y solicitudes recibidas).
   * Formulario para publicar nuevos oficios con tarifa y descripción.
   * Listado de servicios del prestador con distintivos de estado (*Activo* e *Inactivo*) y acciones (*Editar*, *Desactivar*, *Activar*).

6. **Panel de administración - Dashboard (`admin-dashboard.html`)**:
   * Barra lateral de navegación con módulos del sistema.
   * 4 tarjetas de indicadores clave (KPIs): Total de usuarios, servicios activos, solicitudes del mes y satisfacción.
   * Gráfico de barras horizontales desarrollado en CSS puro para ilustrar la demanda de oficios en Facatativá.
   * Tabla con las últimas solicitudes registradas y estados (*Completado*, *En Progreso*, *Pendiente*, *Cancelado*).

7. **Gestión de usuarios (`admin-usuarios.html`)**:
   * Barra de filtros para buscar por texto, rol (*Cliente*, *Todero*, *Admin*) y estado (*Activo*, *Inactivo*).
   * Tabla estructurada con ID, nombre, rol, correo, teléfono, municipio, fecha de registro y estado.
   * Botones de acción por fila (*Editar*, *Pausar*, *Activar*).
   * Paginación informativa básica.

---

## 5. Instrucciones para Ejecución Local

No se requiere instalar Node.js, servidores web ni dependencias adicionales. El proyecto funciona de forma 100% estática abriendo los archivos directamente en cualquier navegador moderno (Google Chrome, Mozilla Firefox, Safari, Microsoft Edge).

### Forma 1: Desde el explorador de archivos
1. Abrir la carpeta `webApp-toderos`.
2. Hacer doble clic sobre `index.html` para iniciar la navegación.

### Forma 2: Desde la terminal (macOS)
```bash
# Navegar a la carpeta del proyecto
cd webApp-toderos

# Abrir la pantalla principal en el navegador predeterminado
open index.html
```

---

## 6. Control de Versiones

El proyecto fue gestionado con Git en la rama `feature/maquetacion-html-css`, con commits descriptivos y atómicos:

* `feat: crear estructura inicial de paginas HTML`
* `feat: maquetar inicio de sesion y registro`
* `style: simplificar maquetacion a estilos basicos formativos`
* `feat: mantener isotipo basico TF en encabezado`
* `feat: maquetar busqueda y solicitud de servicios`
* `feat: maquetar pantalla de mis servicios`
* `feat: maquetar panel y gestion de usuarios`
* `docs: documentar proyecto y forma de ejecucion`
