# 🏁 GPX Rally Management System

**GPX Rally Management System** es una aplicación web desarrollada con **Next.js + TypeScript** siguiendo la metodología **Atomic Design**. Esta herramienta está diseñada para gestionar eventos competitivos con roles diferenciados, permitiendo el registro de puntos de control, penalizaciones, clasificación por categoría y visualización detallada de resultados.

---

## 🚀 **Demo en Vivo**

🌐 **Aplicación Desplegada**: [https://gpx-front-8rip.vercel.app/](https://gpx-front-8rip.vercel.app/)

---

## 📦 Tecnologías y herramientas principales

* **Framework:** [Next.js](https://nextjs.org/)
* **Lenguaje:** TypeScript
* **Estilos:** Tailwind CSS
* **Diseño de componentes:** Atomic Design (Atoms, Molecules, Organisms)
* **Íconos:** Iconify React
* **Backend:** Está contenido en otro repositorio

---

## 🧱 Estructura del Proyecto

El proyecto sigue una arquitectura basada en Atomic Design:

```
/components
  /atoms        -> Botones, tipografías, iconos
  /molecules    -> Tarjetas, filas de datos, secciones con título + contenido
  /organisms    -> Secciones completas: Sidebar, Layout, Secciones de perfil
/pages          -> Rutas principales (index, login, eventos, resultados...)
/context        -> EventContext para compartir datos de eventos entre vistas
/public         -> Imágenes usadas en las vistas
```

---

## 🚀 Instalación del Proyecto

1. **Clona el repositorio:**

   ```bash
   git clone https://github.com/GPX-PI/GPX-Front
   cd gpx-front
   ```

2. **Instala las dependencias:**

   ```bash
   npm install
   ```

3. **Levanta el servidor de desarrollo:**

   ```bash
   npm run dev
   ```

4. **Variables de entorno:**
   Esta configuración se encuentra en el repositorio correspondiente al Backend

---

## 🔐 Sistema de Login

El login está diseñado para permitir ingreso solo a usuarios autorizados, como jueces o encargados del control.

* Los usuarios se cargan desde la base de datos.
* Si el usuario es válido, se redirige a la vista `/controlPointRegister`.
* Si no lo es, se muestra un mensaje de error sin cambiar de vista.

---

## 🧩 Componentes Clave

### ✨ Atoms

* `Button`: Componente reutilizable con variantes de color, tamaño e iconos.

### 🧠 Molecules

* `UserCard`: Tarjeta de perfil con botones personalizables.
* `CompetenceRow`: Fila de resultados o clasificaciones.
* `VideoCard`: Tarjeta con video y datos de video, toma URL de youtube y muestra el video.
* `PriceRow`: Fila de costos con soporte para despliegue de múltiples entradas.

### 🧳 Organisms

* `Layout`: Estructura base para la aplicación.
* `ControlPointRegister`: Vista para registrar paso de participantes.
* `UpcomingEvents`: Vista con tarjetas de eventos próximos.
* `EventDetails`: Descripción de un evento seleccionado.
* `ResultsTable`: Tabla con resultados por categoría.

---

## 🖥️ Vistas Principales

* `/` Inicio
* `/login` Ingreso de jueces autorizados
* `/controlPointRegister` Registro de punto de control
* `/penaltyRegister` Registro de penalizaciones
* `/results` Vista general de resultados
* `/results/[category]` Clasificación por categoría
* `/upcoming-events` Eventos próximos y detalles

---

## 📱 Responsividad

* Sidebar oculta en resoluciones pequeñas y desplegable mediante botón.
* Componentes adaptativos con `flex`, `grid`, `gap`, `min-h`, `overflow`, etc.
* Textos, botones y tablas adaptados a móvil, tablet y escritorio.

---


## 🛠️ En desarrollo futuro...

* Gráficos en tiempo real de resultados y movimientos
* Panel administrativo para control general

---

## 🤝 Contribuciones

Toda mejora es bienvenida. Puedes crear un `Pull Request` o abrir un `Issue` para discutir nuevas funcionalidades o reportar errores.

---

## 📄 Licencia

MIT License. Puedes usarlo, modificarlo y adaptarlo libremente.
