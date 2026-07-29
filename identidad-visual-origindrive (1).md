# Identidad visual — OriginDrive

> Complementa a `especificacion-tecnica-web-club.md`. Este documento define **cómo se ve** el theme; el otro define **qué hace**. Paleta definitiva: **Midnight Navy** (sustituye a los combos "Ocean Blue" y "Racing Green" explorados antes).

## 1. Punto de partida

- Nombre: **OriginDrive**
- Colores de marca definitivos — combo fondo/letra **Midnight Navy**: `#131F33` (fondo) + `#C9D6E3` (letra sobre ese fondo)
- Tipografía: **Inter**, variante **Bold 700 Italic** para el wordmark y titulares
- Estilo: minimalista/elegante
- El combo es reversible, como muestra tu referencia: fondo navy + texto claro (el wordmark grande), o fondo claro + texto navy (la versión pequeña del logo sobre fondo crema). Con este navy tan oscuro, el contraste es excelente en ambas direcciones y a cualquier tamaño de texto — no hace falta ningún ajuste de legibilidad como sí habría hecho falta con el azul medio anterior.

## 2. Paleta de color

| Token | Hex | Uso |
|---|---|---|
| `--origin-navy` | `#131F33` | Color de marca. Fondo del wordmark/hero, botones y enlaces sobre fondo claro, texto de las tarjetas de logo pequeñas |
| `--origin-ice` | `#C9D6E3` | Pareja del navy. Texto sobre fondos navy (wordmark, etiquetas, chips) |
| `--ink` | `#131F33` | Texto principal — se reutiliza el propio navy, no hace falta un negro aparte |
| `--slate` | `#57687A` | Texto secundario, metadatos, fechas |
| `--paper` | `#FFFFFF` | Fondo base |
| `--fog` | `#F0F4F8` | Fondo de sección alterna, más claro que `--origin-ice` |
| `--mist-line` | `#DCE3EA` | Bordes, divisores |
| `--success` | `#2F7D5E` | Plazas disponibles |
| `--warning` | `#B8862B` | Últimas plazas |
| `--error` | `#B23B3B` | Aforo completo |

**Modo oscuro** (reutiliza el propio navy como superficie elevada, en vez de inventar un gris aparte):

| Token | Hex | Nota |
|---|---|---|
| `--paper-dark` | `#0F1826` | Un escalón más oscuro que el navy de marca |
| `--fog-dark` | `#131F33` | El navy de marca pasa a ser la superficie de tarjetas/secciones alternas |
| `--ink-dark` | `#C9D6E3` | Mismo tono ice que en claro |
| `--slate-dark` | `#93A4B3` | |
| `--origin-navy` (dark) | `#6E90B3` | Se aclara para que enlaces/botones se vean sobre fondo oscuro; el navy "puro" ya está ocupado como fondo |
| `--mist-line-dark` | `#26333F` | |

## 3. Tipografía

Inter Bold 700 Italic reservado para wordmark y titulares grandes; el cuerpo usa Inter 400/500, énfasis de UI en 600. (Igual que antes — esta parte no cambia con el color.)

| Rol | Fuente | Uso |
|---|---|---|
| Display/marca | Inter 700 Italic | Wordmark, hero, titulares de sección |
| Énfasis UI | Inter 600 | Tarjetas, botones, subtítulos |
| Cuerpo | Inter 400/500 | Párrafos, navegación, formularios |
| Eyebrow/meta | Inter 500 mayúsculas, `letter-spacing: 0.08em` | Tipo de evento, fechas |

## 4. Espaciado y layout

Sin cambios respecto a la versión anterior: escala de 8px (`4·8·16·24·32·48·64·96·128`), contenedor máx. 1200px, radio de esquina mínimo, sombras muy sutiles. El espacio en blanco generoso sigue siendo lo que sostiene el "elegante".

## 5. La firma visual: "la placa"

Bloque rectangular `--origin-navy` sólido con wordmark o etiqueta en Inter Bold Italic `--origin-ice` centrado y padding generoso — exactamente el tratamiento de tu referencia. Se repite a dos escalas:
- Grande: lockup de marca en el header y bloque principal del hero
- Pequeña: etiqueta de tipo de evento en cada tarjeta, cinta de "Coche del mes"

Con este navy, ya no hace falta invertir la combinación en las etiquetas pequeñas por contraste (como sí habría convenido con el azul medio anterior) — navy de fondo + ice de texto funciona igual de bien a 12px que a 72px.

## 6. Componentes clave

- **Botón primario**: fondo `--origin-navy`, texto `--origin-ice`, sin sombra, radio 4px
- **Botón secundario**: borde 1px `--origin-navy`, texto `--origin-navy`, fondo transparente
- **Tarjeta de evento**: imagen → eyebrow "placa" pequeña → título H3 → fecha/ubicación en `--slate` → contador de plazas en `--success`/`--warning`/`--error`
- **Foco de teclado**: outline 2px `--origin-navy` (o `--origin-ice` en modo oscuro) en todos los elementos interactivos
