# CT Seals — Panel de Inventario

Dashboard web para gestión de inventario de productos hidráulicos y neumáticos.  
Desarrollado para **CT Seals Perú** · [ctseals.com](https://ctseals.com)

---

## Características

- **KPIs en tiempo real** — total de productos, stock crítico, agotados y valor del inventario
- **Gráfico de barras** por categoría y **gráfico de dona** por estado
- **Búsqueda y filtros avanzados:**
  - Búsqueda de texto libre (nombre, código, categoría)
  - Filtro por categoría, estado y unidad de medida
  - Rango de precio unitario
  - Rango de stock actual
  - Rango de fecha de última actualización
- **Ordenamiento** por cualquier columna (clic en encabezado)
- **Exportar a Excel** — genera `.xlsx` con inventario filtrado + hoja de resumen
- **Alertas prioritarias** — productos agotados o bajo mínimo
- **Dark mode** por defecto, diseño responsivo

---

## Estructura del proyecto

```
ct-seals-inventario/
├── index.html       # Dashboard completo (archivo único)
└── README.md        # Este archivo
```

---

## Cómo usar

### Opción 1 — Abrir directamente
Descarga `index.html` y ábrelo en cualquier navegador moderno. No requiere servidor ni instalación.

### Opción 2 — GitHub Pages (recomendado)
1. Sube este repositorio a GitHub
2. Ve a **Settings → Pages**
3. En *Source*, selecciona `main` → `/ (root)`
4. Guarda. En unos segundos tendrás una URL pública:  
   `https://TU_USUARIO.github.io/ct-seals-inventario/`

---

## Actualizar los datos de inventario

Los productos están definidos en el array `productos` dentro de `index.html`.  
Cada producto tiene la siguiente estructura:

```js
{
  cod:    "SH-001",               // Código único
  nombre: "Sello hidráulico 50mm",// Nombre del producto
  cat:    "Sellos Hidráulicos",   // Categoría
  und:    "pza",                  // Unidad (pza, kit, m, lt, kg)
  stock:  38,                     // Stock actual
  min:    10,                     // Stock mínimo
  precio: 28.50,                  // Precio unitario en S/
  fecha:  "2026-05-01"            // Fecha de última actualización (YYYY-MM-DD)
}
```

---

## Tecnologías usadas

| Librería | Uso |
|----------|-----|
| [SheetJS (xlsx)](https://sheetjs.com/) | Exportar Excel |
| [Tabler Icons](https://tabler.io/icons) | Iconografía |

Sin frameworks. HTML + CSS + JavaScript puro.

---

## Capturas

> Agregar capturas del dashboard aquí después de desplegarlo.

---

## Licencia

Uso interno — CT Seals Perú © 2026
