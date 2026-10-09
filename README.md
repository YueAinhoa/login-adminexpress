# 🌸 AdminExpress – Login Responsive

Actividad en clase: armado web de un componente de **Login** usando **HTML, CSS (Grid) y Media Queries**. El diseño es responsive y se adapta a móviles, tabletas y escritorios.

---

## 📑 Índice

1. [Descripción del proyecto](#1-descripción-del-proyecto)
2. [Demo en vivo](#2-demo-en-vivo)
3. [Vista previa](#3-vista-previa)
4. [Tecnologías utilizadas](#4-tecnologías-utilizadas)
5. [Estructura del proyecto](#5-estructura-del-proyecto)
6. [Estructura HTML y Grid](#6-estructura-html-y-grid)
7. [Media Queries (diseño responsive)](#7-media-queries-diseño-responsive)
8. [Paleta de colores](#8-paleta-de-colores)
9. [Tipografía e iconos](#9-tipografía-e-iconos)
10. [Cómo ejecutar el proyecto](#10-cómo-ejecutar-el-proyecto)
11. [Cumplimiento de la actividad](#11-cumplimiento-de-la-actividad)
12. [Autor](#12-autor)

---

## 1. Descripción del proyecto

Este proyecto replica un diseño de página de inicio de sesión para la marca **AdminExpress**. Incluye:

- Panel de marca con el nombre de la aplicación.
- Formulario con campos de **Email** y **Password**.
- Enlace de recuperación de contraseña (*Forgot password?*).
- Botón **Sign In**.
- Enlace de registro (*Sign Up*) visible en la versión móvil.
- Botón de ojo para mostrar u ocultar la contraseña.

El enfoque de desarrollo es **mobile first**: primero se diseña la versión móvil y luego se agregan estilos para pantallas más grandes mediante Media Queries.

---

## 2. Demo en vivo

🔗 **GitHub Pages:** https://TU-USUARIO.github.io/login-adminexpress/

📂 **Repositorio:** https://github.com/TU-USUARIO/login-adminexpress

---

## 3. Vista previa

| Escritorio | Tablet | Móvil |
|---|---|---|
| ![Escritorio](img/escritorio.png) | ![Tablet](img/tablet.png) | ![Móvil](img/movil.png) |

---

## 4. Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| **HTML5** | Estructura semántica de la página |
| **CSS3** | Estilos, variables CSS y animaciones de transición |
| **CSS Grid** | Distribución en columnas del layout principal |
| **Flexbox** | Alineación interna de campos y formulario |
| **Media Queries** | Adaptación a distintos tamaños de pantalla |
| **Google Fonts** | Tipografía Raleway |
| **Bootstrap Icons** | Iconos de sobre, candado y ojo |

---

## 5. Estructura del proyecto

```
login-adminexpress/
├── index.html      → Estructura de la página
├── styles.css      → Estilos y media queries
├── img/            → Capturas de pantalla
└── README.md       → Documentación del proyecto
```

---

## 6. Estructura HTML y Grid

El contenedor principal `.login` es un **CSS Grid** con dos secciones hijas:

```
main.login   (display: grid)
 ├── section.brand   → Panel de color con "AdminExpress"
 └── section.panel   → Formulario de inicio de sesión
      └── div.box
           ├── h2 (título)
           ├── p.subtitle
           └── form
                ├── div.field (Email)
                ├── div.field (Password)
                ├── a.forgot
                ├── button.btn
                └── p.signup
```

**Comportamiento del Grid según la pantalla:**

| Pantalla | Configuración del Grid |
|---|---|
| Móvil | `grid-template-columns: 1fr` (una columna, el panel de marca se oculta) |
| Tablet | `grid-template-rows: 220px 1fr` (banner arriba y formulario abajo) |
| Escritorio | `grid-template-columns: 1fr 1fr` (dos columnas iguales) |

---

## 7. Media Queries (diseño responsive)

Se utilizan **breakpoints** con `min-width` (mobile first) y uno de `max-width` para pantallas muy pequeñas.

| Breakpoint | Rango | Cambios principales |
|---|---|---|
| **Base** | Móvil (< 768px) | Una columna, sin etiquetas visibles, botón de ancho completo, se muestra "Sign Up" |
| `@media (min-width: 768px)` | Tablet | Aparece el banner de marca, se muestran las etiquetas de los campos y se oculta "Sign Up" |
| `@media (min-width: 1024px)` | Escritorio | Dos columnas lado a lado y botón compacto |
| `@media (max-width: 360px)` | Móviles pequeños | Se reduce el tamaño del título y el padding |

Y la etiqueta imprescindible en el `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

## 8. Paleta de colores

La paleta se define con **variables CSS** en `:root`, por lo que se puede cambiar desde un solo lugar.

| Uso | Variable | Color |
|---|---|---|
| Rosa principal (panel, botón, enlaces) | `--blue` | `#c2185b` |
| Rosa hover del botón | — | `#a01049` |
| Texto principal (vino) | `--navy` | `#4a0e2e` |
| Texto secundario | `--gray` | `#8a6b7a` |
| Fondo | `--bg` | `#fdf4f7` |

---

## 9. Tipografía e iconos

- **Fuente:** [Raleway](https://fonts.google.com/specimen/Raleway) (pesos 400, 500, 600 y 700).
- **Iconos:** [Bootstrap Icons](https://icons.getbootstrap.com/) (`bi-envelope`, `bi-lock`, `bi-eye-slash`).

---

## 10. Cómo ejecutar el proyecto

**Opción 1: abrir directamente**
1. Descarga o clona el repositorio.
2. Abre `index.html` con tu navegador.

**Opción 2: clonar con Git**
```bash
git clone https://github.com/TU-USUARIO/login-adminexpress.git
cd login-adminexpress
```
Luego abre `index.html`, o usa la extensión **Live Server** de VS Code (clic derecho → *Open with Live Server*).

**Probar el diseño responsive:** abre las herramientas de desarrollador (`F12`), activa el modo dispositivo (`Ctrl + Shift + M`) y prueba con 375px, 768px y 1280px de ancho.

---

## 11. Cumplimiento de la actividad

| Criterio | Puntos | Cómo se cumple |
|---|---|---|
| **Estructura con HTML y Grid** | 1 pt | HTML semántico (`main`, `section`, `form`, `label`) y layout con `display: grid` y `grid-template-columns` |
| **Uso de Media Queries** | 1 pt | Breakpoints en 768px, 1024px y 360px que cambian el layout y los elementos visibles |

---

## 12. Autor

**Tu Nombre Completo**
Curso: *(nombre de la materia)*
Docente: *(nombre del profesor)*
Fecha: *(fecha de entrega)*

📧 tu-correo@ejemplo.com
🐙 [github.com/TU-USUARIO](https://github.com/TU-USUARIO)
