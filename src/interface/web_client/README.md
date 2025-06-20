# React Web Client

This directory contains a small React interface built with [Vite](https://vitejs.dev/) and TypeScript. It fetches disruption forecast results from the API and renders a Plotly chart.

## Setup

```bash
cd src/interface/web_client
npm install
npm run dev       # start the development server
npm run build     # build production assets in `dist/`
```

The app expects the FastAPI server on `http://localhost:8000`. After running `npm run build`, open `dist/index.html` or copy the `dist/` folder into your container image.

When building the Docker image from the project root, ensure `npm --prefix src/interface/web_client run build` completes so that `src/interface/web_client/dist/` exists. The `infrastructure/Dockerfile` copies this directory automatically.

A basic smoke test simply runs `npm test`, which exits successfully if the project dependencies are installed.
