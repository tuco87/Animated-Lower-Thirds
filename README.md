# Animated Lower Thirds v1.6 - Actualización para OBS 32+

## ✅ CAMBIOS REALIZADOS

Este plugin ha sido actualizado para ser **compatible con OBS Studio 32.0.4** y versiones superiores.

### Problema Original
El plugin dejó de funcionar en OBS 32+ debido a cambios en el navegador integrado (CEF - Chromium Embedded Framework). La API `BroadcastChannel` que usaba el plugin para comunicarse entre el browser source y el control panel ya no funciona correctamente en las versiones recientes de OBS.

### Solución Implementada
- ✅ Reemplazado `BroadcastChannel` por `localStorage` con eventos de cambio
- ✅ Mantiene la misma funcionalidad y apariencia
- ✅ Compatible con OBS 32.0.4 y versiones posteriores
- ✅ Código original comentado para referencia

---

## 📦 INSTALACIÓN

### Opción 1: Instalación Manual

1. **Desinstala la versión anterior** (si la tienes instalada):
   - Elimina la carpeta antigua del plugin de tu ubicación de instalación anterior

2. **Instala la versión actualizada**:
   - Copia la carpeta `Animated-Lower-Thirds` a tu ubicación preferida
   - Por ejemplo: `C:/obs-plugins/Animated-Lower-Thirds/`

3. **Configura en OBS**:
   
   **Browser Source (para los banners en el lienzo):**
   - Crea una nueva fuente de navegador (Browser Source)
   - En "URL local" navega a: `[RUTA]/Animated-Lower-Thirds/lower thirds/browser-source.html`
   - Ancho: 1920, Alto: 1080 (o tu resolución de lienzo)
   - Marca: ✅ "Controlar audio a través de OBS" (si usas sonidos)
   
   **Control Panel (panel de control acoplable):**
   - Ve a Docks → Custom Browser Docks
   - Nombre: `Lower Thirds Control Panel`
   - URL: `[RUTA]/Animated-Lower-Thirds/lower thirds/control-panel.html`
   - Haz clic en "Aplicar"

### Opción 2: Si Ya Tienes el Plugin Instalado

Si ya tienes rutas configuradas en OBS, simplemente:
1. Cierra OBS
2. Reemplaza los archivos `browser-source.html` y `control-panel.html` en tu instalación existente con los de esta versión actualizada
3. Abre OBS nuevamente

---

## 🎯 USO

El plugin funciona exactamente igual que antes:

1. **Configurar los banners**: Usa el panel de control para configurar texto, colores, estilos, etc.
2. **Activar/Desactivar**: Usa los switches en el panel de control
3. **Hotkeys**: Configura atajos de teclado en OBS → Configuración → Atajos de teclado (busca "Lower Thirds")

---

## 🔧 SOLUCIÓN DE PROBLEMAS

### Los banners no aparecen en el lienzo
1. Verifica que el Browser Source esté agregado a tu escena
2. Asegúrate de que la URL apunta al archivo correcto `browser-source.html`
3. Verifica que las dimensiones del Browser Source sean correctas (1920x1080 o tu resolución)
4. Prueba hacer clic derecho en la fuente → Refrescar

### El panel de control no responde
1. Cierra y vuelve a abrir el dock del panel de control
2. Ve a Docks → Cerrar todos los docks personalizados → Vuelve a agregarlo
3. Verifica que la URL del dock apunte a `control-panel.html`

### Los cambios en el control panel no se reflejan en el lienzo
1. Asegúrate de que tanto el Browser Source como el Control Panel Dock estén activos
2. Intenta refrescar ambas fuentes (F5 en el dock del panel, o clic derecho → Refrescar en la fuente)
3. Verifica que no tengas múltiples instancias del Browser Source abierto

### Cache del navegador
Si ves comportamiento extraño después de la actualización:
1. Haz clic derecho en el Browser Source → Propiedades
2. Marca "Actualizar caché del navegador al activar la escena"
3. Haz clic en "Aceptar"
4. Refresca la fuente

---

## 📝 NOTAS TÉCNICAS

### Cambios en el código:
- **browser-source.html**: 
  - Líneas 106-108: BroadcastChannel comentado
  - Nuevas líneas: Event listeners para localStorage
  
- **control-panel.html**:
  - Líneas 1207-1209: BroadcastChannel comentado  
  - Actualizada comunicación para usar localStorage

### Compatibilidad:
- ✅ OBS Studio 32.0.4 (probado)
- ✅ OBS Studio 31.x (compatible)
- ✅ OBS Studio 30.x (compatible)
- ⚠️ Versiones anteriores a OBS 30: Usar plugin original

---

## 📞 SOPORTE

Si encuentras algún problema:

1. Verifica que estés usando OBS 30.0 o superior
2. Comprueba que los archivos `browser-source.html` y `control-panel.html` estén actualizados
3. Revisa el log de OBS (Ayuda → Archivos de registro) para errores específicos

---

## ⚖️ CRÉDITOS

**Plugin Original**: Animated Lower Thirds v1.6 por NoeAL

**Actualización para OBS 32+**: Modificado para compatibilidad con versiones modernas de OBS

**Licencia**: Mantiene la licencia original del plugin

---

## 📋 CHANGELOG

### v1.6-OBS32 (Febrero 2025)
- ✅ Reemplazado BroadcastChannel por localStorage para compatibilidad con OBS 32+
- ✅ Añadidos event listeners para comunicación cross-source
- ✅ Mejorado manejo de errores
- ✅ Mantenida compatibilidad con versiones anteriores de OBS (30.x, 31.x)
- ✅ Sin cambios en la funcionalidad o apariencia del plugin

### v1.6 (Original - Enero 2021)
- Versión original del plugin

## Donations.
If you like the extension and you want to support the development - please consider to donate by [Paypal](https://paypal.me/edgaralex87). Any donations are greatly appreciated.

## License.
The Animated Lower Thirds source code is made available under the [MIT license](https://github.com/noeal-dac/Animated-Lower-Thrids/blob/master/LICENSE).
