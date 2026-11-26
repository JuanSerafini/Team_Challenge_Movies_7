# Catálogo de películas · Team Challenge 7

**Equipo 7:** Giselle Garcia, Carlos Moreno y Juan Gonzalez Serafini.

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones

| Nombre | Rol | Notebook / tarea |
|---|---|---|
| Giselle Garcia | Integración con APIs | `03_tmdb.ipynb` y `04_gemini.ipynb` |
| Carlos Moreno | Analista de datos | `02_analisis.ipynb` (apartados 3 y 4) |
| Juan Gonzalez Serafini | Responsable del repositorio y datos | `01_ingesta_limpieza.ipynb`, apartado 5 de `02_analisis.ipynb` y README |

## Instalación

Clonar el repositorio:

```bash
git clone https://github.com/JuanSerafini/Team_Challenge_Movies_7.git
cd Team_Challenge_Movies_7
```

Crear el entorno virtual:

```bash
python -m venv .venv
```

Activar el entorno virtual:

```bash
# Windows (Git Bash)
source .venv/Scripts/activate

# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Linux / macOS
source .venv/bin/activate
```

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

Crear el archivo `.env` a partir de la plantilla:

```bash
cp .env.example .env
```

Introducir las claves personales de TMDB y Gemini en el archivo `.env` y seleccionar el entorno virtual `.venv` como kernel de los notebooks.

## Claves necesarias

| Variable | Dónde se obtiene |
|---|---|
| `TMDB_READ_ACCESS_TOKEN` o `TMDB_API_KEY` | https://www.themoviedb.org/ → Settings → API |
| `GEMINI_API_KEY` | https://aistudio.google.com/ |

**Importante:** las claves de las APIs deben almacenarse en el archivo `.env`, excluido del control de versiones mediante `.gitignore`. Nunca deben publicarse en GitHub ni aparecer en las salidas de los notebooks.

## Ejecución

Ejecutar los notebooks en el siguiente orden:

1. `01_ingesta_limpieza.ipynb`: ingesta y limpieza de datos. Genera `movies_clean.csv`.
2. `02_analisis.ipynb`: unión de tablas, agregaciones, segmentación de usuarios y análisis de datos.
3. `03_tmdb.ipynb`: enriquecimiento de películas mediante la API de TMDB. Genera `movies10.csv`.
4. `04_gemini.ipynb`: generación de sinopsis en español mediante Gemini. Genera `movies10_es.csv`.

Los archivos CSV generados se almacenan en `data/processed/`.

## Resultados principales

1. Más allá de los conocimientos técnicos adquiridos, lo más enriquecedor ha sido trabajar en equipo simulando un entorno profesional real, utilizando la terminal, Git y GitHub para gestionar ramas, commits, Pull Requests y revisiones de código de forma colaborativa.

2. La integración con APIs nos ha permitido comprender la importancia de proteger las credenciales de acceso y evitar su exposición en el código, en las salidas de los notebooks y en repositorios públicos.

3. El proyecto nos ha enseñado la importancia de inspeccionar, validar y comprender los datos antes de analizarlos, formular preguntas y extraer conclusiones.