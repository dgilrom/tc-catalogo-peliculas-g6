# Catálogo de películas · Team Challenge

> Renombrad este fichero a `README.md` y completad las partes entre `<...>`.

**Equipo:** <Daniel Gil>, <Constante Fernandez>, <Daría Bayko>

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones

| Persona | Rol | Notebook / tarea |
|---|---|---|
| Daniel Gil | Repo y datos | 01_ingesta_limpieza |
| Constante Fernandez | Análisis | 02_analisis|
| Daría Bayko | APIs e IA generativa | 03_tmdb y 04_gemini |

## Instalación

```bash
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
