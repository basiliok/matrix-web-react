# matrix-web-react

Frontend en **React + TypeScript** que permite ingresar una matriz, obtener su **factorización QR** desde `matrix-qr-api-go` y ver las estadísticas que calcula `matrix-stats-api-node`.

> En construcción: por ahora solo muestra una página base.

## Stack

- React 19 + TypeScript
- Vite 8
- Tailwind CSS 4
- ESLint + Prettier (con orden automático de clases de Tailwind)

## Requisitos

- Node.js 24 o superior

## Correr en local

```bash
npm install
npm run dev        # http://localhost:3001
```

## Scripts

| Script            | Descripción                                                   |
| ----------------- | ------------------------------------------------------------- |
| `npm run dev`     | Servidor de desarrollo en el puerto 3001                      |
| `npm run build`   | Verifica los tipos y genera el build de producción en `dist/` |
| `npm run preview` | Sirve el build de `dist/` para revisarlo en local             |
| `npm run lint`    | Revisa el código con ESLint                                   |

Para formatear todo el proyecto: `npx prettier --write .`

## Despliegue

Se publica en **Azure Static Web Apps**. `public/staticwebapp.config.json` redirige cualquier ruta a `index.html` para que la navegación del frontend funcione al recargar la página.

## Repositorios del sistema

| Repositorio                                                                | Rol                                                     | Tecnología                     |
| -------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------ |
| [matrix-qr-api-go](https://github.com/basiliok/matrix-qr-api-go)           | API de factorización QR (punto de entrada del frontend) | Go + Fiber                     |
| [matrix-stats-api-node](https://github.com/basiliok/matrix-stats-api-node) | API de estadísticas sobre las matrices Q y R            | Node.js + Express + TypeScript |
| [matrix-web-react](https://github.com/basiliok/matrix-web-react)           | Frontend                                                | React + TypeScript             |
