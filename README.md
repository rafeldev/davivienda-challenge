# Challenge Davivienda

## Requisitos Previos

- Node.js (v18 o superior)
- Docker y Docker Compose
- npm o yarn

## Ejecución

### 1. Base de Datos (Docker)

Desde la carpeta `davivienda-back`:

```bash
cd davivienda-back
docker-compose up -d
```

Esto iniciará PostgreSQL en un contenedor Docker.

### 2. Backend

Desde la carpeta `davivienda-back`:

```bash
cd davivienda-back
npm install
npm run start:dev
```

El backend estará disponible en `http://localhost:3000`

### 3. Frontend

Desde la carpeta `davivienda-challenge`:

```bash
cd davivienda-challenge
npm install
npm run dev
```

El frontend estará disponible en `http://localhost:5173` (puerto por defecto de Vite)

## Variables de Entorno

Si necesitas configurar variables de entorno, crea un archivo `.env` en `davivienda-back` con:

```
POSTGRES_USER=tu_usuario
POSTGRES_PASSWORD=tu_contraseña
POSTGRES_DB=davivienda_user
POSTGRES_PORT=5432
PORT=3000
```

## Orden de Ejecución Recomendado

1. Iniciar Docker (PostgreSQL)
2. Iniciar Backend
3. Iniciar Frontend

