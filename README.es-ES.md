

# Interstitial Journal

Un complemento de Obsidian que proporciona comandos rápidos para [el diario intersticial](https://nesslabs.com/interstitial-journaling) en tus notas diarias. Inserta entradas con marca de tiempo usando un atajo de teclado en lugar de escribirlas a mano.

## Comandos

### Agregar entrada de diario intersticial

Inserta una entrada con marca de tiempo y deja el cursor listo para que escribas:

```
- 14:30 - your note here
```

### Agregar entrada de diario intersticial con nueva página

Inserta una entrada con marca de tiempo y un enlace wiki, dejando el cursor dentro de los corchetes para que escribas el nombre de la página:

```
- 14:30 - [[2026-02-26 your page name]]
```

## Detección inteligente de líneas

Ambos comandos son conscientes del contexto de la línea actual:

- **Línea vacía** -- inserta la entrada en la línea actual.
- **Marcador de lista sin contenido** (por ejemplo, Obsidian continuó automáticamente una viñeta hasta `- `) -- agrega la marca de tiempo después del marcador existente sin duplicarlo (solo formato de viñeta).
- **Línea con contenido existente** -- inserta la entrada en una nueva línea abajo, preservando la sangría.

## Configuración

| Configuración | Predeterminado | Opciones |
|---------------|----------------|----------|
| Formato de hora | `HH:mm` | Cualquier cadena de [formato de Moment.js](https://momentjs.com/docs/#/displaying/format/) (por ejemplo, `hh:mm A` para formato de 12 horas) |
| Formato de fecha | `YYYY-MM-DD` | Cualquier cadena de formato de Moment.js para la fecha en los enlaces wiki de nueva página |
| Estilo de hora | Normal | **Normal** (`14:44`) o **Negrita** (`**14:44**`) |
| Separador | Guion | **Guion** (`-`), **Dos puntos** (`:`), **Flecha** (`>`), **Barra** (`/`), **Barra vertical** (`\|`) o **Ninguno** |
| Formato de entrada | Lista con viñetas | **Lista con viñetas** (`- `) o **Texto plano** (sin prefijo) |

## Instalación

### Manual

1. Copia `main.js` y `manifest.json` en tu bóveda en `.obsidian/plugins/interstitial-journal/`.
2. Recarga Obsidian.
3. Habilita **Interstitial Journal** en **Configuración -> Complementos de la comunidad**.

### Desarrollo

```bash
npm install
npm run dev    # watch mode
npm run build  # production build
```

## Atajos de teclado

Después de habilitar el complemento, asigna los atajos de teclado en **Configuración -> Atajos de teclado** buscando "Interstitial Journal".
