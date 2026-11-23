# 00 · Documento de inicio del proyecto

## 1. Datos del alumno/a

| | |
|---|---|
| **Nombre** (real o alias, como prefieras: [por qué](publicacion-y-privacidad.md)) | Marcos Sánchez Morocho |
| **Usuario de GitHub** | marcosSanchezMorocho |
| **Repositorio del proyecto** | https://github.com/marcosSanchezMorocho/proyecto-final-daw-marcos-sanchez-morocho |
| **Ciclo y curso** | DAW, 2.º · curso 2026-27 |
| **Fecha** | 2026-11-17 |

## 2. Nombre del proyecto

**Mesa Virtual de Rol** — plataforma web para partidas de rol en tiempo real entre varios jugadores, con gestión de fichas, tableros, dados y memoria de campaña.

## 3. Qué quiero hacer

Quiero construir una aplicación web que permita jugar partidas de rol a distancia con amigos: cada jugador tiene su ficha de personaje, hay un tablero compartido, se pueden hacer tiradas de dados y todo lo que ocurre queda guardado como memoria de la campaña para retomarla entre sesiones. El juego es en tiempo real, por lo que varios jugadores interactúan a la vez sobre la misma partida. Se usará definitivamente una IA como máster de la partida. El plan es empezar con un modo de un solo jugador (un jugador humano + máster IA) y, si el tiempo lo permite, añadir después el modo multijugador con varios jugadores humanos compartiendo la misma partida. El núcleo (fichas, dados, tablero y memoria) se entrega primero y debe ser completo por sí solo.

## 4. Qué problema o necesidad resuelve

Jugar rol requiere juntarse físicamente y un máster que conduzca la partida, lo que dificulta mantener campañas cuando los jugadores viven lejos o tienen horarios distintos. Además, la información de la campaña (personajes, eventos, decisiones) se pierde entre sesiones si no se anota bien. Esta aplicación resuelve ambas cosas: permite jugar online en tiempo real y conserva la memoria de la campaña para retomarla. La necesidad la conozco por experiencia propia jugando con amigos a distancia.

## 5. Para quién

Jugadores de rol y másteres que quieran partidas online, especialmente grupos de amigos dispersos geográficamente. También personas que quieran jugar en solitario mediante el máster con IA. Uso personal/asociativo, no empresarial.

## 6. Funcionalidades principales

| # | Funcionalidad | ¿Imprescindible? (sí / no) |
|---|---|---|
| 1 | Fichas de personaje (creación, edición y consulta) | sí |
| 2 | Tiradas de dados con resultados compartidos en tiempo real | sí |
| 3 | Tablero compartido con posiciones de personajes | sí |
| 4 | Memoria de la campaña persistente entre sesiones | sí |
| 5 | Juego en tiempo real multijugador (WebSockets) | sí |
| 6 | Máster con IA (definitivo; primero modo un jugador, después multijugador) | sí |

## 7. Tecnologías previstas

| Tecnología | Para qué | Nivel actual (nada / algo / bien) |
|---|---|---|
| React | Interfaz de usuario (fichas, tablero, chat) | algo |
| WebSockets | Comunicación en tiempo real entre jugadores | algo |
| Base de datos vectorial | Memoria de la campaña y búsqueda semántica | nada |
| API de un LLM | Máster con IA (ampliación) | algo |
| Docker | Despliegue y entorno reproducible | algo |
| Backend (Node.js/Python) | API, lógica de negocio y persistencia | bien |

## 8. Dónde se integra con los módulos de 2.º

- [x] Desarrollo web en entorno cliente (0612)
- [x] Desarrollo web en entorno servidor (0613)
- [x] Despliegue de aplicaciones web (0614)
- [x] Diseño de interfaces web (0615)

## 9. Datos y empresas

- ¿El proyecto parte de una **empresa**? **No**. Es un proyecto personal.
- ¿Usará **datos personales reales**? **No**: se usarán datos de ejemplo (personajes y campañas ficticias).

## 10. Riesgos y dudas iniciales

Lo que más me preocupa es el máster con IA: mantener la coherencia y el ritmo en campañas largas puede complicarse mucho, así que empezaré por el modo de un solo jugador y dejaré el multijugador humano como mejora posterior. Otros riesgos: la sincronización en tiempo real entre jugadores, el diseño de la base de datos vectorial para la memoria y el tiempo disponible para llegar a la primera versión mínima antes del 31 de marzo.

## 11. Qué espero aprender

Espero aprender a construir aplicaciones en tiempo real con WebSockets, a usar bases de datos vectoriales y a integrar APIs de LLM, además de mejorar en Docker y en el diseño de interfaces con React.

---

## Aprobación del tutor

*Esta parte la rellena el tutor.*

| Criterio mínimo | Cumple |
|---|---|
| Necesidad real y documentada | ☐ |
| Alcance abordable en el tiempo disponible | ☐ |
| Integra contenidos de al menos tres módulos de 2.º | ☐ |
| No usa datos personales reales | ☐ |

**Estado:** ☐ Aprobada · ☐ Aprobada con cambios · ☐ Necesita rehacerse

**Fecha:** 

**Comentarios del tutor:**