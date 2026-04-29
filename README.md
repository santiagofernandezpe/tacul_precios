# Tacul Indumentaria — Lista de Precios Web

App web offline para consultar y buscar precios de Tacul Indumentaria.

---

## 🚀 Cómo subir a GitHub Pages (una sola vez)

### Paso 1 — Crear cuenta en GitHub
1. Ir a [github.com](https://github.com) y crear una cuenta gratuita
2. Confirmar el email

### Paso 2 — Crear un repositorio
1. Hacer clic en el botón verde **"New"** (o el ícono "+")
2. Nombre del repositorio: `tacul-precios` (todo en minúsculas, sin espacios)
3. Seleccionar **"Public"**
4. Hacer clic en **"Create repository"**

### Paso 3 — Subir los archivos
1. En la página del repositorio recién creado, hacer clic en **"uploading an existing file"**
2. Arrastrar los 4 archivos de esta carpeta:
   - `index.html`
   - `precios.json`
   - `sw.js`
   - `manifest.json`
3. Hacer clic en **"Commit changes"**

### Paso 4 — Activar GitHub Pages
1. Ir a **Settings** (pestaña superior del repositorio)
2. En el menú izquierdo, hacer clic en **"Pages"**
3. En "Source", seleccionar **"Deploy from a branch"**
4. En "Branch", seleccionar **"main"** y carpeta **"/ (root)"**
5. Hacer clic en **"Save"**
6. Esperar 1-2 minutos y la URL aparece arriba (ej: `https://tunombre.github.io/tacul-precios`)

---

## 💰 Cómo actualizar precios (el proceso más importante)

1. Abrir el archivo `precios.json` con el Bloc de Notas (Windows) o cualquier editor de texto
2. Buscar el producto por su código (ej: `"codigo": "GA-001"`)
3. Cambiar el número después de `"precio_efectivo":` (ej: `4500` → `5200`)
4. Guardar el archivo
5. Volver a GitHub, ir al repositorio, hacer clic en `precios.json`
6. Hacer clic en el ícono del lápiz ✏️ (editar)
7. Cambiar los precios directamente ahí
8. Hacer clic en **"Commit changes"**
9. En 30 segundos el sitio se actualiza en todos los dispositivos

**El precio lista (tarjeta) se calcula solo — solo hay que cambiar `precio_efectivo`.**

---

## 📱 Instalar como app en el celular

Una vez que el sitio esté en GitHub Pages:
1. Abrir la URL en Chrome (Android) o Safari (iPhone)
2. Android: menú → "Añadir a pantalla de inicio"
3. iPhone: botón compartir → "Añadir a pantalla de inicio"

La app funciona offline después de la primera visita.

---

## 📁 Agregar un producto nuevo al `precios.json`

Copiar este bloque y pegarlo dentro de la lista `"productos"`, antes del último `]`:

```json
,
{ 
  "codigo": "XX-000", 
  "descripcion": "Nombre del producto", 
  "categoria": "Uniformes Escolares", 
  "talles": ["S","M","L","XL"], 
  "colores": ["Blanco"], 
  "unidad": "Un", 
  "precio_efectivo": 0000 
}
```

Categorías disponibles: `"Uniformes Escolares"` · `"Gastronomía / Hotelería"` · `"Mantenimiento"`
