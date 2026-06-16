# Catálogo de Flores 🌸

Página de catálogo en un solo archivo (`index.html` + carpeta `images/`).
Funciona abriéndola directo en el navegador o subiéndola a GitHub Pages.

## Lo primero que tenés que cambiar

Abrí `index.html`, buscá el bloque **CONFIG** (casi al final, dentro de `<script>`):

```js
const CONFIG = {
  marca:     "Flores de Montaña",   // nombre del negocio
  lema:      "...",                 // frase de la portada
  whatsapp:  "50600000000",         // <-- NÚMERO REAL: 506 + 8 dígitos, sin + ni espacios
  ubicacion: "Costa Rica",
};
```

El número de WhatsApp va sin `+`, sin espacios ni guiones. Ej: `50688887777`.
Cada botón "Pedir" abre el chat con un mensaje ya escrito con el nombre de la flor.

## Agregar una flor nueva

1. Meté la foto en la carpeta `images/` (idealmente recortada y no muy pesada).
2. En el bloque **FLORES**, copiá una línea y cambiala:

```js
{ nombre:"Geranio Blanco", categoria:"Geranios", img:"images/geranio-blanco.jpg", detalle:"Flor blanca", precio:"₡2.500" },
```

- `categoria`: usá una de las que ya existen (Geranios, Coleos, Petunias, Torenias, Begonias)
  para que herede los cuidados. Si inventás una nueva, agregale su entrada en el bloque **CUIDADOS**.
- `precio`: dejalo `""` y aparece "Consultar", o poné el monto.

Los chips de categoría y los contadores se actualizan solos.

## Cuidados

El texto de luz/riego/duración sale del bloque **CUIDADOS** según la categoría.
Es una **guía general** — revisalo con la vendedora antes de publicar.

## Subir a GitHub Pages

1. Creá un repo y subí `index.html` y la carpeta `images/`.
2. Settings → Pages → Branch `main` / carpeta `/root` → Save.
3. En un par de minutos queda en `https://USUARIO.github.io/REPO/`.

## Categorías incluidas

- **Geranios** (6): fucsia, vino, rojo, lila, coral, rosa
- **Coleos** (8): follaje ornamental, varias combinaciones
- **Petunias** (3): rosa, doble fucsia, doble blanca
- **Torenias** (1): flor de la suerte
- **Begonias** (1): rosa
