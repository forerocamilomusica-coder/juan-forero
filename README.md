# Museo Virtual VR con A-Frame

## 📱 Descripción del Proyecto

Este es un **museo virtual inmersivo en realidad virtual (VR)** desarrollado con **A-Frame**, una plataforma de código abierto para crear experiencias VR accesibles en navegadores web. El museo presenta una escultura abstracta geométrica como objeto principal de exhibición, con iluminación profesional tipo galería y controles interactivos.

### Obra Principal Exhibida

**Holismos 5**  
Artista: Candela Muniozguren  
Material: Acero lacado  
Dimensiones: 29 × 35 × 30 cm  
Año: 2024  
Tipo: Escultura abstracta geométrica

---

## 🚀 Cómo Usar

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Para VR: Dispositivo compatible (Cardboard, Oculus, HTC Vive, etc.) o gafas VR
- Para desktop: Solo necesitas tu computadora y un navegador

### Pasos para Abrir el Museo

1. **Abrir el archivo HTML**
   - Localiza el archivo `museo_vr.html` en tu carpeta
   - Abre con un navegador web (haz doble clic o arrastra a la ventana del navegador)

2. **Permitir acceso al dispositivo**
   - En algunos navegadores, deberás permitir acceso al sensor de orientación
   - Acepta los permisos cuando te lo pida

3. **Entrar en VR (opcional)**
   - Si tienes un dispositivo VR compatible, busca el botón de "Realidad Virtual" (ícono de gafas VR) en la esquina inferior derecha
   - Coloca tu teléfono en las gafas VR
   - ¡Disfruta de la experiencia inmersiva!

---

## 🎮 Controles

### Movimiento y Vista

| Acción | Control |
|--------|---------|
| Caminar adelante | `W` o Flecha arriba |
| Caminar atrás | `S` o Flecha abajo |
| Moverse izquierda | `A` o Flecha izquierda |
| Moverse derecha | `D` o Flecha derecha |
| Girar la vista | Ratón o joystick |
| Acercarse (Zoom in) | Scroll del ratón hacia arriba |
| Alejarse (Zoom out) | Scroll del ratón hacia abajo |

### Interacción

| Acción | Control |
|--------|---------|
| Ver información de la obra | Click en la escultura |
| Cerrar información | Click de nuevo en la escultura |

---

## 🏛️ Características del Museo

### Arquitectura
- **Piso**: Cerámica oscura (#1a1a1a) con acabado realista
- **Paredes**: Cemento pulido gris oscuro (#1f1f1f) - ambiente tipo galería profesional
- **Techo**: Minimalista para crear sensación de amplitud

### Iluminación (Tipo Galería Profesional)

La iluminación está diseñada para resaltar la escultura y crear un ambiente inmersivo:

1. **Luz Ambiental** (intensity: 0.3)
   - Proporciona base de iluminación general
   - Color blanco puro

2. **Luz Direccional** (intensity: 0.7)
   - Simula luz natural desde frontal-superior
   - Posición: (3, 3, 4)

3. **Spotlight Principal** (intensity: 1.8)
   - Resalta la escultura y sus colores
   - Posición: (0, 2.2, 2)

4. **Luz Complementaria Lateral** (intensity: 0.6)
   - Luz azulada que realza volúmenes
   - Proporciona profundidad

### Pedestal de Museo
- Base cilíndrica elegante (#2a2a2a)
- Anillo decorativo superior dorado (#4a4a4a)
- Material con acabado metalizado
- Centrado en el espacio de exhibición

### La Escultura Abstracta: Holismos 5

Composición geométrica moderna con 6 planos de acero lacado:

1. **Plano Base Azul Oscuro** (#0052CC)
   - Base inclinada horizontal
   - Proporciona estabilidad visual

2. **Plano Oro/Amarillo** (#FFD700)
   - Plano diagonal frontal-superior
   - Tono cálido y luminoso

3. **Elemento Azul Brillante** (#0066FF)
   - Plano vertical lateral
   - Contraste cromático fuerte

4. **Plano Rojo** (#FF3333)
   - Plano inclinado frontal
   - Punto focal de color primario

5. **Plano Rosa Suave** (#FFB6D9)
   - Plano horizontal posterior
   - Tono pastel complementario

6. **Oro Oscuro** (#B8860B)
   - Elemento complementario
   - Armonía cromática cálida

**Características de Animación:**
- Rotación suave continua (0-30 grados)
- Flotación delicada (± 0.12 unidades en eje Y)
- Efectos visuales al seleccionar

---

## 🖱️ Panel Informativo

Al hacer click en la escultura, aparece un panel con información:

```
🎨 Holismos 5
Artista: Candela Muniozguren
Técnica: Acero lacado
Dimensiones: 29 × 35 × 30 cm
Año: 2024
Tipo: Escultura abstracta
```

El panel es interactivo y se puede cerrar haciendo click nuevamente o en el botón "Cerrar".

---

## 🎨 Personalización y Edición

### Editar Colores de la Escultura

Busca en el código cada plano y modifica el valor `color`:

```html
<!-- Ejemplo: cambiar color del plano azul oscuro -->
color="#0052CC"  →  color="#FF6600"  (cambia a naranja)
```

### Editar Materiales (Brillo y Textura)

Modifica las propiedades de material:

```html
material="metalness: 0.7; roughness: 0.3;"
```

- **metalness**: 0-1 (0=mate, 1=espejo brillante)
- **roughness**: 0-1 (0=pulido, 1=áspero)

### Editar Escala de la Escultura

Modifica el `scale` del contenedor:

```html
<a-entity scale="0.8 0.8 0.8">
```

Ejemplos:
- `scale="1 1 1"` - Tamaño normal
- `scale="1.5 1.5 1.5"` - 50% más grande
- `scale="0.5 0.5 0.5"` - 50% más pequeña

### Editar Posición

Modifica el `position`:

```html
<a-entity position="0 0.3 0">
```

Formato: `position="X Y Z"`
- X: movimiento izquierda (-) / derecha (+)
- Y: movimiento abajo (-) / arriba (+)
- Z: movimiento atrás (-) / adelante (+)

### Editar Rotación

Modifica el `rotation`:

```html
<a-entity rotation="0 30 0">
```

Formato: `rotation="X Y Z"` (en grados 0-360)
- X: rotación eje X
- Y: rotación eje Y (más común para rotar alrededor)
- Z: rotación eje Z

### Editar Iluminación

**Cambiar intensidad de luz:**

```html
<a-light intensity="1.8">  →  <a-light intensity="2.5">
```

**Cambiar posición de luz:**

```html
<a-light position="0 2.2 2">  →  <a-light position="1 3 3">
```

**Cambiar color de luz:**

```html
<a-light color="#ffffff">  →  <a-light color="#ffff00">
```

---

## 📁 Estructura del Archivo

```
museo_vr.html
├── <head>
│   ├── Meta tags (charset, viewport)
│   ├── A-Frame librería (1.5.0)
│   └── Estilos CSS (panel informativo)
│
├── <body>
│   ├── <a-scene> (escena principal)
│   │   ├── Arquitectura (piso, paredes, techo)
│   │   ├── Iluminación (4 luces)
│   │   ├── Pedestal
│   │   ├── Escultura (6 planos geométricos)
│   │   └── Cámara
│   │
│   ├── Panel de información (HTML)
│   │
│   └── <script>
│       ├── Variables de zoom
│       ├── Control de zoom (scroll)
│       ├── Interactividad (click)
│       └── Animaciones
```

---

## 🔧 Herramientas Utilizadas

- **A-Frame 1.5.0**: Framework WebVR/VR para navegadores
- **HTML5**: Estructura del documento
- **CSS3**: Estilos del panel informativo
- **JavaScript**: Lógica de interactividad y controles
- **WebGL**: Renderizado 3D
- **Three.js**: Motor 3D subyacente (utilizado por A-Frame)

---

## 🌐 Compatibilidad

| Dispositivo | Soporte |
|------------|---------|
| Desktop (Chrome, Firefox) | ✅ Completo |
| Tablet (iPad, Android) | ✅ Completo |
| Smartphone VR (Cardboard) | ✅ Completo |
| Oculus Quest/Rift | ✅ Completo |
| HTC Vive | ✅ Completo |
| PlayStationVR | ⚠️ Limitado |
| Safari | ✅ Básico |

---

## 📚 Recursos Adicionales

### Documentación oficial
- [A-Frame Documentation](https://aframe.io/docs/)
- [A-Frame Entity Component System](https://aframe.io/docs/1.5.0/core/entity.html)

### Tutoriales
- [A-Frame School - Lessons](https://aframe.io/school/)
- [WebVR Experiments](https://webvr.info/)

### Comunidad
- [A-Frame Slack Community](https://aframevr.slack.com/)
- [A-Frame GitHub](https://github.com/aframevr/aframe)

---

## 🎯 Ideas para Expandir el Proyecto

1. **Múltiples Obras de Arte**
   - Añadir más esculturas en diferentes áreas del museo
   - Crear galerías temáticas

2. **Navegación Mejorada**
   - Sistema de waypoints (puntos de interés)
   - Minimap para orientación
   - Guía de audio (audioguía)

3. **Interactividad Avanzada**
   - Rotación manual de obras (drag & drop)
   - Cambio de iluminación por usuario
   - Galería de imágenes de alta resolución

4. **Realismo Visual**
   - Texturas detalladas
   - Sombras dinámicas
   - Reflejos y refracciones

5. **Experiencias Sociales**
   - Multiplayer (múltiples visitantes simultáneamente)
   - Chat en VR
   - Tours guiados

6. **Estadísticas y Análisis**
   - Tracking de tiempo de vista por obra
   - Heatmaps de navegación
   - Engagement metrics

---

## 📝 Changelog

### Versión 1.0 (Febrero 2, 2026)
- ✅ Escena base del museo virtual
- ✅ Arquitectura (piso, paredes, iluminación)
- ✅ Escultura abstracta "Holismos 5"
- ✅ Pedestal de museo
- ✅ Sistema de información interactivo
- ✅ Controles de movimiento y zoom
- ✅ Animaciones de flotación y rotación

---

## 📄 Licencia

Este proyecto utiliza A-Frame que está bajo licencia MIT.

---

## 👨‍💼 Créditos

**Desarrollo**: Proyecto de Realidad Virtual  
**A-Frame**: Mozilla VR Team  
**Obra Exhibida**: "Holismos 5" - Candela Muniozguren (2024)  
**Concepto**: Museo Virtual Inmersivo  

---

## 📞 Soporte

Para reportar errores o sugerencias:
1. Abre el archivo en tu navegador
2. Abre la consola del navegador (F12)
3. Verifica mensajes de error
4. Revisa la documentación de A-Frame

---

**Última actualización:** Febrero 2, 2026  
**Versión de A-Frame:** 1.5.0
