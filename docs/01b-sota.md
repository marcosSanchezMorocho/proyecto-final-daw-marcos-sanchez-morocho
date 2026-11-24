# 01b · Estado del arte (SOTA) de mi proyecto

## 1. Problema y preguntas de búsqueda (CE 1c)

**Problema:** Es difícil jugar partidas de rol a distancia manteniendo la inmersión y la memoria de la campaña entre sesiones.

| # | Pregunta | Dónde busqué | Fecha |
|---|---|---|---|
| P1 | ¿Qué soluciones VTT existen y qué ofrecen? | Google, tiendas de apps, GitHub | 2026-11-17 |
| P2 | ¿Cómo ganan dinero las plataformas de rol online? | Sitios oficiales, Wikipedia | 2026-11-17 |
| P3 | ¿Qué tecnologías usan para tiempo real y memoria? | Documentación técnica, blogs | 2026-11-17 |
| P4 | ¿Existe algún máster con IA para rol? | Búsqueda web, Product Hunt | 2026-11-17 |
| P5 | ¿Qué hueco deja el mercado para mi proyecto? | Comparativa de soluciones | 2026-11-17 |

## 2. Soluciones existentes (CE 1a, 1c, 2a)

| Solución | Para quién | Qué hace | Modelo de precio | Enlace y fecha de acceso | Estado |
|---|---|---|---|---|---|
| Roll20 | Jugadores y másteres online | VTT completo: fichas, mapas, dados, tienda | Freemium + suscripción | https://roll20.net (17-11-2026) | leído |
| Foundry VTT | Másteres que quieren autoalojar | VTT muy extensible por módulos | Licencia única | https://foundryvtt.com (17-11-2026) | leído |
| Fantasy Grounds | Grupos con reglas oficiales | VTT con automatización de reglas | Licencia + suscripción | https://www.fantasygrounds.com (17-11-2026) | leído |
| D&D Beyond | Jugadores de D&D | Fichas digitales y compendio | Freemium + suscripción | https://www.dndbeyond.com (17-11-2026) | leído |
| Owlbear Rodeo | Grupos que quieren algo simple | VTT minimalista de mapas | Gratuito | https://www.owlbear.rodeo (17-11-2026) | leído |
| AI Dungeon | Jugadores en solitario | Narrativa interactiva con IA | Freemium | https://aidungeon.io (17-11-2026) | leído |
| Hoja de cálculo / papel | Cualquiera | Notas y fichas manuales | Gratuito | N/A | leído |

## 3. Modelos de negocio (CE 1d, 1e)

| Patrón | Soluciones que lo usan | Ventaja | Riesgo |
|---|---|---|---|
| Freemium | Roll20, D&D Beyond, AI Dungeon | Capta usuarios gratis | Conversión baja |
| Suscripción | Roll20, Fantasy Grounds | Ingresos recurrentes | Churn |
| Licencia única | Foundry VTT | Pago único atractivo | Menos ingresos recurrentes |
| Gratuito | Owlbear Rodeo | Alta adopción | Difícil de monetizar |

Mi proyecto no es un negocio: es un proyecto académico. Si fuera producto, seguiría un modelo freemium con el núcleo gratuito y funciones avanzadas (máster IA) de pago.

## 4. Herramientas y tecnologías (CE 2a, 2b)

| Decisión | Opción | Madurez | Licencia | Coste | Curva de aprendizaje | Encaje con el ciclo | Elegida |
|---|---|---|---|---|---|---|---|
| Frontend | React | Alta | MIT | Gratuito | Media | Sí (cliente) | Sí |
| Tiempo real | WebSockets (Socket.IO) | Alta | MIT | Gratuito | Media | Sí (servidor) | Sí |
| BD vectorial | Chroma / Pinecone | Media | OSS / pago | Bajo | Media | No directo | Sí (Chroma) |
| LLM | OpenAI API | Alta | Comercial | Por uso | Baja | No directo | Sí |
| Despliegue | Docker | Alta | Apache 2.0 | Gratuito | Media | Sí (despliegue) | Sí |
| Backend | Node.js + Express | Alta | MIT | Gratuito | Baja | Sí (servidor) | Sí |

## 5. Hueco y diferenciación (CE 1e)

Roll20 es un VTT completo (fichas, mapas, dados, tienda) y en la tabla no aparece un máster con IA para quien no quiere hacer de máster.

AI Dungeon ofrece narrativa interactiva con IA y en la tabla no se presenta como un VTT con fichas, mapas y dados conectados.

Mi proyecto aporta un núcleo ligero con memoria persistente y máster IA, primero para un jugador y después para multijugador.

En mi opinión, Owlbear Rodeo sigue siendo mejor para un máster que domina su sistema y quiere un VTT minimalista; Roll20 y D&D Beyond, para grupos con máster humano que usan sistemas y compendios preparados.

En mi opinión, AI Dungeon sigue siendo mejor para quien quiere jugar en solitario con un sistema basado en texto.

## 6. Decisiones derivadas (CE 1e, 1f, 2b)

- **Tipo de proyecto elegido**: aplicación web ligera de rol en tiempo real con máster IA (enlace apartado 3 de 01-analisis.md).
- **Requisitos que salen del estudio**: RF-02 (tiradas compartidas), RF-04 (memoria), RF-06 (máster IA), RNF-01 (latencia <1 s).
- **Decisiones técnicas**: React + WebSockets + Chroma + OpenAI API + Docker + Node/Express (ver decisiones/).

## 7. Fuentes y calidad (CE 2a)

| # | Fuente (enlace) | Tipo | Fecha de acceso | Fiabilidad |
|---|---|---|---|---|
| F1 | https://roll20.net | Sitio oficial | 17-11-2026 | Alta |
| F2 | https://foundryvtt.com | Sitio oficial | 17-11-2026 | Alta |
| F3 | https://www.fantasygrounds.com | Sitio oficial | 17-11-2026 | Alta |
| F4 | https://www.dndbeyond.com | Sitio oficial | 17-11-2026 | Alta |
| F5 | https://www.owlbear.rodeo | Sitio oficial | 17-11-2026 | Alta |
| F6 | https://aidungeon.io | Sitio oficial | 17-11-2026 | Media |

## 8. Límites

- No se han probado las plataformas de pago (solo documentación pública).
- Los precios pueden variar; se tomaron de los sitios oficiales en la fecha indicada.
- No se verificó el rendimiento real de las BD vectoriales con datos de campaña.

---

## Criterios de evaluación que alimenta este documento (texto literal)

- **1a)** Se han clasificado las empresas del sector por sus características organizativas y el tipo de producto o servicio que ofrecen.
- **1c)** Se han identificado las necesidades más demandadas a las empresas.
- **1d)** Se han valorado las oportunidades de negocio previsibles en el sector.
- **1e)** Se ha identificado el tipo de proyecto requerido para dar respuesta a las demandas previstas.
- **1f)** Se han determinado las características específicas requeridas al proyecto.
- **2a)** Se ha recopilado información relativa a los aspectos que van a ser tratados en el proyecto.
- **2b)** Se ha realizado el estudio de viabilidad técnica del mismo.

> El SOTA **no añade criterios de evaluación**: reúne en un solo sitio lo que 1a-1f y 2a-2b ya piden. La evaluación sigue las listas de cotejo de H1 y H2.