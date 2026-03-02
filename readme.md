# PMA_SJN.HTML — Formato de Control de Obras en Campo (PMA)

## 📋 Descripción

Este archivo HTML es un **formato digital editable** para el **Plan de Manejo Ambiental (PMA)**, diseñado para uso en obra civil.  
Permite registrar el cumplimiento de actividades ambientales, calcular automáticamente el porcentaje de cumplimiento, adjuntar evidencias fotográficas y generar un PDF listo para impresión.

El diseño está optimizado para:

- 💻 Computador (uso en oficina)
- 📱 Celular / tablet (uso en campo)
- 🖨️ Impresión en tamaño carta / A4

---

## 🧱 Estructura general

El documento está dividido en:

1. **Encabezado**
   - Logos (Alcaldía / Consorcio)
   - Datos generales:
     - Contratista
     - Fecha
     - HSEQ / SISO

2. **Resumen automático**
   - ✔️ Cantidad de CUMPLE
   - ❌ Cantidad de NO CUMPLE
   - 📊 % de cumplimiento (calculado automáticamente)

3. **Tarjetas PMA**
   - PMA-001 — Uso eficiente del agua
   - PMA-002 — Manejo de residuos sólidos
   - Cada medida incluye:
     - Estado (Cumple / No cumple / N/A)
     - % de avance (0–100)
     - Observaciones
     - Galería / Cámara (adjuntar imágenes)

4. **Firmas**
   - Firma Interventor / Supervisor
   - Firma Residente / Contratista

5. **Botones flotantes**
   - Generar PDF
   - Limpiar formulario

---

## ⚙️ Funcionalidades principales

### 1) Cálculo automático de cumplimiento

La función `calc()`:

- Cuenta estados CUMPLE y NO CUMPLE.
- Suma porcentajes de avance.
- Divide SIEMPRE entre **8 ítems** (regla solicitada).
- Limita valores entre 0 y 100.
- Muestra el resultado en el resumen.

Ejemplo:

- 1 actividad con 100% → 12.5%
- 2 actividades con 100% → 25%

---

### 2) Carga de logos

Función:

```js
loadLogo(input)
```

Permite seleccionar una imagen y mostrarla como fondo del recuadro del logo.

---

### 3) Galería de fotos

Función:

```js
previewImages(input)
```

- Permite seleccionar varias imágenes.
- Muestra miniaturas.
- Se pueden eliminar haciendo clic sobre la imagen.

El input nativo está oculto para mantener el diseño visual.

---

### 4) Impresión optimizada

Se usa:

```css
@media print
```

Para:

- Ocultar botones y controles innecesarios.
- Mantener colores.
- Ajustar márgenes.
- Evitar saltos de página dentro de tarjetas.
- Mantener el diseño igual que en pantalla.

---

## 🎨 Personalización rápida

### Cambiar colores principales

Editar variables CSS:

```css
:root{
 --primary:#004d40;
 --secondary:#d84315;
}
```

---

### Cambiar tamaño del botón Galería / Cámara

```css
.upload-zone{
  font-size:22px;
}
```

---

### Centrar elementos del resumen

```css
.pma-resumen div{
  display:flex;
  justify-content:center;
  align-items:center;
}
```

---

## 🖨️ Recomendaciones para PDF

- Usar opción **Guardar como PDF** del navegador.
- Activar:
  - Escala automática
  - Fondos gráficos (si está disponible)
- Tamaño carta o A4.

---

## 📁 Archivos

- `PMA_SJN.HTML` → archivo principal editable.
- No requiere librerías externas.
- Funciona completamente offline.

---

## 🧰 Tecnologías usadas

- HTML5
- CSS3 (Grid + Media Queries)
- JavaScript Vanilla (sin frameworks)

---

## 👷 Uso recomendado en obra

1. Abrir el HTML en navegador.
2. Llenar información del día.
3. Adjuntar evidencias.
4. Revisar % cumplimiento automático.
5. Generar PDF.
6. Firmar digital o imprimir.

---

## ✨ Notas

- El diseño prioriza velocidad y compatibilidad.
- No necesita internet.
- Compatible con Chrome, Edge y Safari.

---

## 📌 Autoría

Documento generado y ajustado para uso práctico en campo según requerimientos del proyecto PMA.
