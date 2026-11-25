# Catálogo de películas · Team Challenge 7

> Renombrad este fichero a `README.md` y completad las partes entre `<...>`.

**Equipo: 7** <Giselle Garcia>, <Carlos Moreno>, <Juan Gonzalez Serafini>

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones
| Nombre | Rol | Notebook / tarea |
|---|---|---|
| Giselle Garcia | Integración con APIs | `03_tmdb.ipynb` y `04_gemini.ipynb` |
| Carlos Moreno | Analista de datos | `02_analisis.ipynb` |
| Juan Gonzalez Serafini | Responsable de repo y datos | `01_ingesta_limpieza.ipynb` |

## Instalación

```bash
git clone <URL del repo>
cd <carpeta>
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env            # y rellenad las claves
```

## Claves necesarias

| Variable | Dónde se obtiene |
|---|---|
| `TMDB_READ_ACCESS_TOKEN` o `TMDB_API_KEY` | themoviedb.org → Settings → API |
| `GEMINI_API_KEY` | aistudio.google.com |

## Ejecución

Ejecutad los notebooks **en este orden** (cada uno genera un CSV en `data/processed/` que usa el siguiente):

1. `01_ingesta_limpieza.ipynb` → `movies_clean.csv`
2. `02_analisis.ipynb`
3. `03_tmdb.ipynb` → `movies10.csv`
4. `04_gemini.ipynb` → `movies10_es.csv`

## Resultados principales

<3–5 frases con lo más interesante que habéis encontrado>

1. Más allá de los conocimientos técnicos adquiridos, lo más enriquecedor ha sido trabajar en equipo simulando un entorno profesional real, utilizando la terminal, Git y GitHub para gestionar ramas, commits, Pull Requests y revisiones de código de forma colaborativa
2. Cada vez que imprimía algo para comprobar que funcionaba la conexión  a la API de Tmdb salia mi contraseña y después tenía que borrar esos prints para no dejar rastro
Conclusión hay que tener cuidado con lo que públicas si usas contraseñas
3. Nos dejó una regla simple: primero inspeccioná, validá y comprendé los datos; después actua, preguntá y construí