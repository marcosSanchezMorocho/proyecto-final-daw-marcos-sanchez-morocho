# Mesa Virtual de Rol

Aplicación web para partidas de rol en tiempo real entre varios jugadores, con gestión de fichas de personaje, tableros, tiradas de dados y memoria de campaña entre sesiones. Incluye un máster con IA (primero en modo un jugador, después multijugador).

## Estado del proyecto

Proyecto de final de ciclo (DAW, 2.º). En fase de análisis y documentación inicial (H1). Primera versión mínima prevista antes del 31-03-2027.

## Tecnologías previstas

- Frontend: React
- Tiempo real: WebSockets (Socket.IO)
- Backend: Node.js + Express
- Base de datos vectorial: Chroma (memoria de campaña)
- IA: API de un LLM (máster)
- Despliegue: Docker

## Estructura

```
docs/               Documentación del proyecto (00, 01, 01b, ...)
src/                Código fuente (en desarrollo)
tests/              Pruebas
```

## Autor

Marcos Sánchez Morocho — [@marcosSanchezMorocho](https://github.com/marcosSanchezMorocho)

Repositorio: https://github.com/marcosSanchezMorocho/proyecto-final-daw-marcos-sanchez-morocho