# 🇪🇸 Spain API Atlas

Catálogo abierto y colaborativo de **APIs públicas de España**: estatales,
autonómicas y municipales. Lo mantienen personas y agentes de IA autónomos.

## Qué hay aquí

Cada API es un fichero YAML en [`apis/`](apis/). Ejemplo:

```yaml
nombre: AEMET OpenData
organismo: Agencia Estatal de Meteorología
ambito: estatal            # estatal | autonomico | municipal
region: null               # "Andalucía", "Madrid"... si no es estatal
categoria: meteorologia
url_base: https://opendata.aemet.es/opendata/api
docs_url: https://opendata.aemet.es/dist/index.html
auth: apikey               # none | apikey | oauth
formato: json
licencia: https://www.aemet.es/es/nota_legal
ejemplo:
  peticion: GET /prediccion/especifica/municipio/diaria/28079
  respuesta_resumida: '{"estado":200,"datos":"https://..."}'
ultima_verificacion: 2026-09-30
notas: La respuesta devuelve una URL; hay que hacer una segunda petición.
```

El esquema completo está en [`schema.json`](schema.json).

## Cómo contribuir

### Si eres un agente de IA
Lee [`AGENTS.md`](AGENTS.md) y sigue sus reglas al pie de la letra.

### Si eres una persona
1. Haz fork del repo
2. Crea `apis/<slug>.yaml` (slug en minúsculas con guiones, p. ej. `renfe-horarios`)
3. Ejecuta `python scripts/validate.py apis/<slug>.yaml`
4. Abre un PR con **una sola API**

### ¿No tienes tiempo de documentarla?
Abre un issue con la etiqueta `api-sin-documentar` y la URL.
Otro agente o persona la documentará.

## Reglas
- Solo APIs **públicas y legales** de uso. Nada de endpoints privados ni scraping que viole los términos.
- El ejemplo tiene que ser una **llamada real** que funcione en la fecha de `ultima_verificacion`.
- Nada de API keys, tokens ni datos personales en los ficheros.
- Todos los PR pasan la validación automática y una revisión humana.

## Licencia
Datos del catálogo: [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
Cada API tiene su propia licencia, indicada en su fichero.
