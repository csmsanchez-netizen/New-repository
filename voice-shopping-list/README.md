# Lista de Compras por Voz

Aplicación web de una sola página (sin instalación ni servidor) para armar tu lista
semanal de compras usando comandos de voz en español, pensada para tiendas como
Plaza Vea, Tottus, Metro, Wong, Vivanda, etc.

## Cómo usarla

### En línea (GitHub Pages)

GitHub Pages ya está activo en este repositorio (publica la raíz de `main`),
así que la app queda disponible en:

`https://csmsanchez-netizen.github.io/New-repository/voice-shopping-list/`

Ábrela desde el navegador de tu celular o computadora (Chrome o Edge) y úsala
directamente, sin instalar nada.

### Localmente

Abre `index.html` en **Google Chrome o Microsoft Edge** (son los navegadores con
soporte del reconocimiento de voz que usa la app). Se puede abrir directamente
como archivo local o servirlo con cualquier servidor estático.

1. Elige tu acento/idioma en el selector (Perú, Chile, México, etc.).
2. Toca el botón del micrófono 🎤 y di el comando.
3. La app confirma cada acción por voz y actualiza la lista en pantalla al instante.
4. Vuelve a tocar el micrófono para dejar de escuchar.

También puedes agregar y editar productos manualmente desde el formulario y la
tabla (cantidad, unidad y tienda son editables directamente).

## Comandos de voz soportados

| Acción | Ejemplos |
|---|---|
| Agregar producto | "agrega 2 kilos de arroz", "añadir 1 litro de leche en Plaza Vea", "necesito 3 paquetes de fideos" |
| Quitar producto | "quitar leche", "eliminar arroz", "borra los fideos" |
| Modificar cantidad | "cambiar arroz a 5 kilos", "modificar cantidad de leche a 2 litros" |
| Leer la lista | "leer lista", "qué tengo en la lista" |
| Vaciar la lista | "vaciar lista", "borrar toda la lista" |
| Archivar la semana y empezar de nuevo | "nueva semana", "archivar semana" |
| Repetir la lista de la semana pasada | "repetir semana pasada" |

Si dices el nombre de una tienda al final del comando de agregar (por ejemplo
"... en Tottus"), la app etiqueta el producto con esa tienda.

## Datos y almacenamiento

Todo se guarda en el `localStorage` del navegador (no requiere backend ni cuenta):

- La lista activa de la semana.
- El historial de semanas archivadas, para repetir productos recurrentes con un
  clic o por voz ("repetir semana pasada").

Como todo vive en el navegador, la lista es local a ese dispositivo/navegador;
no se sincroniza entre dispositivos.

## Publicación en GitHub Pages

Este repositorio ya tenía GitHub Pages activo (Settings → Pages → "Deploy from
a branch" → `main` → `/root`), así que no hace falta ningún paso adicional:
cualquier cambio que se fusione a `main` dentro de `voice-shopping-list/` se
publica solo en la URL de arriba en uno o dos minutos.

## Limitaciones conocidas

- El reconocimiento de voz del navegador requiere conexión a internet y solo
  funciona en Chrome/Edge (no en Firefox ni Safari).
- La interpretación de comandos es por patrones de texto en español; si un
  comando no se reconoce, la app lo indica por voz y en pantalla para que lo
  repitas o lo hagas manualmente.
