# Catálogo de películas · Team Challenge

**Equipo:** Daniel Gil, Constante Fernández, Daría Bayko

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones

| Persona | Rol | Notebook / tarea |
|---|---|---|
| Daniel Gil | Repo y datos | 01_ingesta_limpieza |
| Constante Fernández | Análisis | 02_analisis |
| Daría Bayko | APIs e IA generativa | 03_tmdb y 04_gemini |

## Instalación

```bash
git clone https://github.com/dgilrom/tc-catalogo-peliculas-g6.git
cd tc-catalogo-peliculas-g6
python -m venv venv

# Activar el entorno
venv\Scripts\activate           # Windows (PowerShell / CMD)
source venv/bin/activate        # Mac / Linux

pip install -r requirements.txt

# Crear el .env a partir de la plantilla y rellenar las claves
copy .env.example .env          # Windows
cp .env.example .env            # Mac / Linux
```

## Claves necesarias

Las claves van solo en el fichero `.env`, que está en el `.gitignore`. Nunca se escriben en los notebooks ni se suben al repositorio.

| Variable | Dónde se obtiene |
|---|---|
| `TMDB_READ_ACCESS_TOKEN` o `TMDB_API_KEY` | themoviedb.org → Settings → API |
| `GEMINI_API_KEY` | aistudio.google.com |

## Ejecución

Ejecutad los notebooks **en este orden**. Cada uno genera un CSV en `data/processed/` que usa el siguiente:

1. `01_ingesta_limpieza.ipynb` → `movies_clean.csv` (añade la columna `year` extraída del título)
2. `02_analisis.ipynb` (merge, agregaciones y preguntas sobre los datos)
3. `03_tmdb.ipynb` → `movies10.csv` (10 películas con `overview` y `homepage` de TMDB)
4. `04_gemini.ipynb` → `movies10_es.csv` (añade `overview_es`, la sinopsis en español)

## Resultados principales

-Muy interesenta trabajar con Git y github, Daniel y Daría nunca habían trabajado en equipo con control de versiones y han aprendido mucho.
Asustaba al principio.. Mergear por error en main o sin aprobación enseña rápido para que sirven las ramas y las PRs revisadas.
- Python como siempre es un trabajo duro. Más aún trabajando con ficheros.
- Cuando al final salen las cosas es un momento de felicidad.