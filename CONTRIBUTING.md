# Contribuir a cely-frontend

## Flujo de trabajo

1. Crea un branch desde `main`: `git checkout -b feat/nombre-feature`
2. Haz tus cambios y commitea con mensajes descriptivos
3. Abre un Pull Request hacia `main`
4. Espera que el CI pase (lint + type-check + build)
5. Solicita revisión de al menos 1 persona del equipo
6. Merge solo después de aprobación y CI verde

## Reglas del branch `main`

- **No push directo** — solo vía Pull Request
- **1 aprobación requerida** antes de hacer merge
- **CI debe estar verde**: lint, type-check y build deben pasar

## Convenciones de código

### Commits

Usamos [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: agregar página de producto
fix: corregir cálculo de precio con IVA
chore: actualizar dependencias
docs: mejorar README
style: formatear componente Cart
refactor: extraer hook useCartTotal
test: agregar tests para página Shop
```

### Código

- **TypeScript estricto** — sin `any` implícito
- **Componentes funcionales** con hooks de React
- **No comentarios obvios** — el código debe ser autoexplicativo
- **Un componente por archivo** — nombre igual al componente
- **Imports absolutos** desde `src/` (configurar en `vite.config.ts`)

### Estructura de archivos

```
src/
├── components/
│   └── NombreComponente/
│       ├── index.tsx       # Componente principal
│       └── NombreComponente.test.tsx
├── pages/
│   └── NombrePagina.tsx
└── hooks/
    └── useNombreHook.ts
```

## Ejecutar antes de cada PR

```bash
npm run lint        # Debe dar 0 errores
npm run type-check  # Debe dar 0 errores
npm run build       # Debe completar sin errores
npm test            # Todos los tests deben pasar
```

## Variables de entorno

Nunca commits archivos `.env*`. Documenta las nuevas variables en el README.

## Preguntas

Abre un Issue o contacta al equipo de desarrollo.
