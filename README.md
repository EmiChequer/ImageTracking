# 🐋 Orca AR - Image Tracking Project

Una aplicación de Realidad Aumentada (AR) que utiliza seguimiento de imágenes para mostrar un modelo 3D animado de una orca con sonido ambiental.

![Orca AR Preview](https://via.placeholder.com/600x300/1e3a8a/ffffff?text=Orca+AR+Experience)

## 🌟 Características

- **Seguimiento de imágenes en tiempo real** usando MindAR
- **Modelo 3D animado** de una orca en formato GLB
- **Audio ambiental** que se reproduce cuando se detecta la imagen objetivo
- **Animaciones fluidas** usando Three.js
- **Experiencia web** sin necesidad de instalación de apps

## 🛠️ Tecnologías Utilizadas

- **A-Frame** - Framework de realidad virtual/aumentada para web
- **MindAR** - Biblioteca de seguimiento de imágenes para AR
- **Three.js** - Motor de gráficos 3D para animaciones
- **WebGL** - Renderizado de gráficos 3D en el navegador
- **HTML5/CSS3/JavaScript** - Tecnologías web estándar

## 📁 Estructura del Proyecto

```
ImageTracking/
├── index.html          # Aplicación principal AR
├── Orca3D.glb         # Modelo 3D de la orca
├── orca-sound.mp3     # Audio ambiental de la orca
├── targets.mind       # Archivo de imagen objetivo para tracking
└── README.md          # Documentación del proyecto
```

## 🚀 Instalación y Uso

### Prerrequisitos

- Navegador web moderno con soporte para WebGL
- Cámara web o dispositivo móvil con cámara
- Conexión a internet (para cargar las librerías CDN)

### Pasos para ejecutar

1. **Clona o descarga** este repositorio
2. **Inicia un servidor local** (requerido para cargar archivos GLB):
   ```bash
   # Usando Python 3
   python -m http.server 8000
   
   # Usando Node.js (si tienes http-server instalado)
   npx http-server
   
   # Usando PHP
   php -S localhost:8000
   ```
3. **Abre tu navegador** y navega a `http://localhost:8000`
4. **Permite el acceso a la cámara** cuando el navegador lo solicite
5. **Apunta la cámara** hacia la imagen objetivo configurada en `targets.mind`
6. **¡Disfruta!** Verás aparecer la orca 3D animada con sonido

## 🎯 Cómo Funciona

### Detección de Imagen
- La aplicación utiliza **MindAR** para detectar una imagen específica en tiempo real
- El archivo `targets.mind` contiene los datos de la imagen objetivo entrenada

### Renderizado 3D
- Cuando se detecta la imagen, aparece el modelo 3D de la orca
- El modelo está posicionado y escalado para aparecer sobre la imagen detectada
- Las animaciones se manejan directamente con **Three.js** para mayor control

### Audio Interactivo
- El sonido ambiental se reproduce automáticamente cuando aparece la orca
- Se detiene cuando se pierde el tracking de la imagen

## 🔧 Configuración Técnica

### Parámetros del Modelo 3D
```javascript
position="0 0.1 0.1"     // Posición relativa a la imagen
rotation="190 90 270"    // Rotación en grados (X, Y, Z)
scale="0.2 0.2 0.2"      // Escala del modelo
```

### Configuración de Audio
```javascript
sound="loop: true; volume: 0.8"  // Audio en bucle con volumen al 80%
```

## 🎨 Personalización

### Cambiar el Modelo 3D
1. Reemplaza `Orca3D.glb` con tu propio modelo
2. Ajusta los parámetros de `position`, `rotation` y `scale` en `index.html`
3. Asegúrate de que el modelo tenga animaciones si quieres mantener esa funcionalidad

### Cambiar la Imagen Objetivo
1. Usa **MindAR Studio** para entrenar una nueva imagen objetivo
2. Reemplaza el archivo `targets.mind` con el nuevo archivo generado
3. La imagen debe tener buen contraste y características distintivas

### Modificar el Audio
- Reemplaza `orca-sound.mp3` con tu archivo de audio preferido
- Ajusta el volumen modificando el parámetro `volume` en el código

## 🌐 Compatibilidad

### Navegadores Soportados
- ✅ Chrome (recomendado)
- ✅ Firefox
- ✅ Safari (iOS 11.3+)
- ✅ Edge

### Dispositivos
- 💻 **Desktop**: Requiere webcam
- 📱 **Móvil**: Android 7+ / iOS 11.3+
- 🥽 **VR/AR**: Compatible con dispositivos WebXR

## 🐛 Solución de Problemas

### El modelo no aparece
- Verifica que estés usando un servidor local (no `file://`)
- Comprueba la consola del navegador para errores
- Asegúrate de que la imagen objetivo esté bien iluminada y visible

### Audio no se reproduce
- Algunos navegadores requieren interacción del usuario antes de reproducir audio
- Verifica que el archivo de audio no esté corrupto
- Comprueba los permisos de audio del navegador

### Tracking inestable
- Mejora la iluminación del entorno
- Mantén la imagen objetivo plana y sin reflejos
- Asegúrate de que la imagen tenga suficiente contraste

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Haz fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📞 Contacto

Si tienes preguntas o sugerencias, no dudes en abrir un issue en este repositorio.

---

**¡Disfruta explorando la realidad aumentada con esta experiencia inmersiva de orca! 🐋✨**