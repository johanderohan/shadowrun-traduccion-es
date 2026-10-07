# Shadowrun (SNES) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/super-nintendo/shadowrun)**.

Traducción al **español de España** de *Shadowrun* (Super Nintendo, 1993), el
RPG ciberpunk de Beam Software publicado por Data East que nunca salió en
español. Se ha traducido desde la versión **estadounidense en inglés**, que es
la original del juego.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia para aplicarlo.

## Estado

Última versión: **[v1.0 — Primera publicación](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion, conversaciones y bocadillos | **1606 de 1606 líneas** traducidas y revisadas |
| Palabras clave («Preguntar..») | 64 de 64 (las 53 que se usan caben en su lista) |
| Menús, objetos, armas, hechizos y estado | Traducidos y medidos en pantalla |
| Terminales de la Matriz, introducción, créditos, título y opciones | Traducidos (66 bloques) |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ñ ¡ ¿ « »** |
| Logotipos (SHADOWRUN, FASA, Data East, Beam) | Se conservan, por ser imagen de marca |
| Revisión durante una partida | Parcial (ver abajo) |

La jerga del universo Shadowrun se mantiene donde forma parte de su identidad
(*chummer*, *drek*, *nuyen*, *decker*, *shadowrunner*) y el resto se adapta
(la Matriz, el hielo, el matasanos, los necrófagos, los Desguaces…). Cada
personaje conserva su voz: los orcos y el Rey hablan con gramática rota,
Hamfist habla de sí mismo en tercera persona, el Bufón se burla con rimas.

### Cambios técnicos

- El texto en castellano ocupa más que el inglés, así que el parche **amplía la
  ROM a 2 MB** (16 Mbit, LoROM) y reubica el texto. Funciona en emuladores y
  flashcarts que admiten ROMs de ese tamaño.
- Los bocadillos tenían un tamaño fijo calculado para el inglés: el parche los
  **agranda automáticamente** cuando el texto no cabe y alarga el tiempo que
  permanecen en pantalla en proporción al texto.
- Fuente con letras españolas nuevas y el mismo color y contraste que el
  original (también en la fuente del título, la de la Matriz y la de la introducción).

### Comprobaciones y trabajo pendiente

- Cada una de las 1606 líneas se vuelve a leer desde la ROM construida y
  coincide con el guion; una auditoría automática comprueba la fuente, los
  parches del motor y los límites de cada ventana.
- Se ha jugado en emulador (snes9x), desde partida nueva y sin trucos, el
  comienzo de la historia hasta los Desguaces: la morgue, la calle, combates,
  el apartamento de Jake, **guardar y cargar partida** (también arrancando en
  frío), el club Grim Reaper, comprar y vender, el teléfono, The Cage y
  Glutman, el Rey y la arena. Esas partidas se jugaron con candidatas
  anteriores (mismo motor y fuente); la versión publicada se ha comprobado
  con una prueba de humo desde partida nueva y repitiendo las pruebas de los
  textos que cambiaron.
- Con pruebas dirigidas (modificando la memoria del emulador) se han visto en
  pantalla todas las palabras clave, todos los objetos, armas, blindajes y
  hechizos, los menús de estado, la agenda del teléfono, las ofertas de compra
  y venta, el premio de la arena, la contratación de runners, los terminales
  de la Matriz y 255 mensajes que el juego elige al vuelo.
- **Pendiente:** una partida completa de principio a fin, el combate real en la
  Matriz, la prueba en consola física y una revisión humana independiente.
  La traducción y su revisión se han hecho con asistencia de IA. Por eso la
  versión figura «en revisión»; si encuentras algo, abre una incidencia.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **USA**. El parche solo funciona con
   esa versión exacta, sin cabecera de copiadora:

   | | |
   |---|---|
   | Archivo | `Shadowrun (USA).sfc` |
   | Tamaño | 1.048.576 bytes (1 MB) |
   | MD5 | `694be8df403ee59225c4b6b53c30fb7b` |
   | CRC32 | `3F34DFF0` |

   ```bash
   md5sum "Shadowrun (USA).sfc"                        # Linux
   md5 "Shadowrun (USA).sfc"                           # macOS
   CertUtil -hashfile "Shadowrun (USA).sfc" MD5        # Windows
   ```

   Si tu archivo mide 1.049.088 bytes tiene una cabecera de 512 bytes: quítala
   antes de parchear. Si el MD5 no coincide, el parche fallará.
3. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Shadowrun (USA).sfc" shadowrun-snes-es-v1.0.xdelta "Shadowrun (ES).sfc"`
4. Comprueba que la ROM resultante mide **2.097.152 bytes** (2 MB) y tiene MD5
   **`a2a4daf2eb8c67452ff25f105d5af1d3`**.
5. Empieza una **partida nueva** en tu emulador o flashcart.

Las partidas guardadas con la versión inglesa no se han probado con la traducida.

## Cambios por versión

### v1.0 — 6 de octubre de 2026

- Primera publicación: guion completo, menús, objetos, Matriz, introducción y
  créditos en castellano de España.
- Fuente española nueva, ROM ampliada a 2 MB y bocadillos que se ajustan al texto.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin
relación alguna con Data East, Beam Software, FASA ni los actuales titulares de
Shadowrun. Aquí no se distribuye el juego ni ninguna parte de él: solo un
parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia
y lo hago.
