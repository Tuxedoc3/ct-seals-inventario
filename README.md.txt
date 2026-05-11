# CT Seals — Catálogo de Materiales

Dashboard web para consulta y gestión del catálogo de materiales prima (MP) de sellos hidráulicos y neumáticos.  
Desarrollado para **CT Seals Perú** · [ctseals.com](https://ctseals.com)

---

## Vista en vivo

🔗 **[https://Tuxedoc3.github.io/ct-seals-inventario/](https://Tuxedoc3.github.io/ct-seals-inventario/)**

---

## Contenido del catálogo

| Familia | Código | Descripción | Artículos |
|---------|--------|-------------|-----------|
| Poliuretano | PU | U500, U510, U550, U575, U585 | ~2,560 |
| Elastómero | EL | NBR, H-NBR, EPDM, FPM, Silicone | ~3,800 |
| Plástico | PL | POM, Poliamida, PTFE (3 tipos) | ~1,200 |
| Material Nacional | MN | Acetal, Poliacetal, Teflon, UHMW... | ~9 |

Cada artículo incluye: **código único**, **descripción**, **diámetro interior (DI)**, **diámetro exterior (DE)** y **longitud** en mm.

---

## Funcionalidades

- **KPIs en tiempo real** — total de artículos, familias, subfamilias y filtrados activos
- **Gráficos** — barras por familia y dona de distribución
- **Búsqueda y filtros avanzados:**
  - Búsqueda libre por código, descripción o material
  - Filtro por familia (PU / EL / PL / MN)
  - Filtro por subfamilia / material (dinámico según familia)
  - Rango de diámetro interior (mm)
  - Rango de diámetro exterior (mm)
  - Rango de longitud (mm)
- **Carga de stock desde Excel** — sube tu archivo con columnas `Código` y `Stock`
- **Exportar a Excel** — genera `.xlsx` con el catálogo filtrado (incluye familia, subfamilia, medidas y stock)
- Tabla con **ordenamiento** por cualquier columna
- Diseño **dark mode**, responsivo

---

## Estructura del repositorio

```
ct-seals-inventario/
├── index.html       # Dashboard completo (archivo único, sin dependencias locales)
└── README.md        # Este archivo
```

---

## Cómo usar

### Abrir localmente
Descarga `index.html` y ábrelo en cualquier navegador moderno. No requiere servidor ni instalación.

### GitHub Pages (en línea)
El sitio se publica automáticamente desde la rama `main`.  
URL: `https://Tuxedoc3.github.io/ct-seals-inventario/`

---

## Cómo actualizar el stock

1. Exporta el catálogo con el botón **Exportar Excel**
2. En el archivo descargado, rellena la columna `Stock` con tus cantidades actuales
3. Guarda el archivo y súbelo al dashboard con **Actualizar stock (Excel)**
4. El sistema cruza automáticamente por código y muestra los valores

El archivo Excel de stock debe tener al menos estas columnas:

| Código | Stock |
|--------|-------|
| PUU5000001 | 15 |
| ELN1070001 | 8 |
| PLT1010001 | 3 |

También acepta columnas como `Qty`, `Cantidad`, `Existencia`, `SKU`, `Ref`.

---

## Tecnologías

| Librería | Uso | Fuente |
|----------|-----|--------|
| [SheetJS (xlsx)](https://sheetjs.com/) | Leer y exportar Excel | CDN |
| [Tabler Icons](https://tabler.io/icons) | Iconografía | CDN |

Sin frameworks. HTML + CSS + JavaScript puro. Un solo archivo.

---

## Fuente de datos

Los datos provienen del archivo **CODIFICACION MP** (catálogo oficial de materiales prima de CT Seals).  
Las medidas en la descripción siguen el formato: `Material - DI / DE / Longitud` (en mm).

---

## Licencia

Uso interno — CT Seals Perú © 2026
