# cely-frontend

Tienda online de Cely Arte y Crochet — interfaz de usuario construida con React 18 + Vite + TypeScript y desplegada en Cloudflare Pages.

## Stack

| Herramienta | Versión | Propósito |
|---|---|---|
| React | 18.x | UI framework |
| Vite | 5.x | Bundler / dev server |
| TypeScript | 5.x | Tipado estático |
| react-router-dom | 6.x | Navegación SPA |
| SWR | 2.x | Data fetching + caché |
| react-i18next | 14.x | i18n ES / EN |
| Zod | 3.x | Validación de esquemas |
| Vitest | 1.x | Testing |

## Requisitos previos

- Node.js 20+
- npm 10+

## Inicio rápido

```bash
npm install
npm run dev        # Dev server en http://localhost:5173
npm run build      # Compilar para producción → dist/
npm run preview    # Previsualizar build local
```

## Scripts disponibles

| Comando | Descripción |
|---|---|
| `npm run dev` | Servidor de desarrollo con HMR |
| `npm run build` | Build de producción (`tsc -b && vite build`) |
| `npm run type-check` | Verificación de tipos sin emitir archivos |
| `npm run lint` | ESLint sobre todos los archivos `.ts/.tsx` |
| `npm test` | Suite de tests con Vitest |

## Estructura del proyecto

```
src/
├── assets/          # Imágenes, fuentes estáticas
├── components/      # Componentes reutilizables
├── pages/           # Páginas por ruta (Home, Shop, Product, Cart, About)
├── hooks/           # Custom hooks (useCatalog, useCart, useConfig)
├── lib/             # Clientes HTTP, helpers
├── locales/         # Traducciones es.json / en.json
├── types/           # Tipos TypeScript compartidos
└── main.tsx         # Punto de entrada
```

## Variables de entorno

Crea un archivo `.env.local` (no lo commits):

```env
VITE_API_URL=https://api.celyarteycrochet.com
VITE_WA_NUMBER=+58XXXXXXXXXX
```

## Despliegue

El CI despliega automáticamente a Cloudflare Pages:

- **Preview:** cada PR genera un preview en `*.cely-crochet.pages.dev`
- **Producción:** push a `main` → `cely-crochet.pages.dev`

## Contribuir

Ver [CONTRIBUTING.md](./CONTRIBUTING.md).
