# 🥁 DrumsAstor

Editor visual de patrones de batería, JSON-based. Sin dependencias, sin build, sin servidor — un solo archivo HTML.

## ✨ Features

- **Editor visual** estilo step-sequencer (Hi-Hat, Snare, Kick) con 8 / 16 / 32 pasos.
- **Drag-to-paint:** click + arrastrar para pintar/borrar varias celdas de una pasada.
- **Audio sintetizado** con Web Audio API (sin samples, no requiere conexión).
- **BPM 40–220** con scheduler look-ahead para timing tight.
- **Modos:** repetir un solo patrón o secuencia automática de todos.
- **JSON-based:** exportá / importá tu sesión como JSON (copiar o descargar `.json`).
- **Auto-guardado** en `localStorage` del navegador.
- **Mobile-friendly:** layout adaptado para celular con touch targets cómodos.
- **Atajos:** `Space` play/stop, `Esc` cierra modal.

## 🚀 Uso

Abrí `index.html` en cualquier navegador moderno. No hay nada que instalar.

O usalo online: **https://dante-militello.github.io/drumsastor/**

## 📦 Formato JSON

```json
{
  "version": 1,
  "title": "Mi sesión",
  "bpm": 90,
  "loopMode": "single",
  "patterns": [
    {
      "title": "Groove base",
      "steps": 16,
      "tracks": {
        "hihat": [1,0,0,0, 1,0,0,0, 1,0,0,0, 1,0,0,0],
        "snare": [0,0,0,0, 1,0,0,0, 0,0,0,0, 1,0,0,0],
        "kick":  [1,0,0,0, 0,0,0,0, 1,0,0,0, 0,0,0,0]
      }
    }
  ]
}
```

- `steps` debe ser `8`, `16` o `32`.
- Cada track (`hihat`, `snare`, `kick`) es un array de 0/1 con exactamente `steps` elementos.
- `loopMode` puede ser `"single"` (repite el patrón actual) o `"sequence"` (cicla por todos).

## 🛠 Stack

HTML + CSS + JS vanilla. Cero dependencias.
