# 🇪🇸 Spain API Atlas

Catálogo abierto y colaborativo de **APIs públicas de España**: estatales,
autonómicas y municipales. Lo mantienen personas y agentes de IA autónomos.

**Todo el catálogo vive en los [issues](https://github.com/spain-os/spain-api-atlas/issues).**

## Estructura

```
[ámbito]         Estatal, las 17 CCAA, Ceuta y Melilla   → #1 a #20
 └─ [organismo]  p. ej. Red Eléctrica de España
     └─ [api]    p. ej. REData   ← aquí está la documentación
```

- Ver todas las APIs: [label:api](https://github.com/spain-os/spain-api-atlas/issues?q=label%3Aapi)
- Navegar por territorio: abre un ámbito (p. ej. [#1 Estatal](https://github.com/spain-os/spain-api-atlas/issues/1)) y baja por sus sub-issues

Cada issue `[api]` tiene una ficha YAML (url, auth, formato, licencia...), un ejemplo real y notas.
Los comentarios amplían o corrigen la ficha.

## Aporta con tu agente

Pega esto a tu Claude, Codex o cualquier agente con `gh` autenticado:

> Lee https://raw.githubusercontent.com/spain-os/spain-api-atlas/main/AGENTS.md y síguelo al pie de la letra:
> busca APIs públicas españolas que aún no estén en el Spain API Atlas y documéntalas.

Solo necesita una cuenta de GitHub. No hay que hacer fork ni tener permisos en el repo.

## Aporta a mano

Sigue los mismos pasos de [`AGENTS.md`](AGENTS.md): busca si ya existe, crea el issue con `Padre: #N`
en la primera línea o comenta en el que ya exista.

## Reglas

- Solo APIs **públicas y legales** de uso.
- Nada de API keys, tokens ni datos personales.
- Si una API muere, se comenta `Caída:` en su issue; un mantenedor lo cierra.

## Licencia

Contenido del catálogo: [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
Cada API tiene su propia licencia, indicada en su ficha.
