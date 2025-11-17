# Proyecto final
**CC3103 - Procesamiento de Lenguaje Natural**

*Clasificación y análisis de sentimiento en comentarios de Reddit.*


Este repositorio contiene notebooks y scripts para enriquecer, preprocesar y modelar comentarios (VADER + modelos clásicos).

**Contenido clave**
- `src/preprocessing.ipynb`: enriquecimiento con VADER y normalización (genera `data/enriched/`).
- `src/baseline.ipynb`: preparación de datos y baseline TF-IDF + SVM.
- `src/model.ipynb`: experimentos con RandomForest, LogisticRegression y LinearSVC.
- `data/raw/`, `data/enriched/`, `data/processed/`: entrada y salidas de cada etapa.

**Requisitos**
- Python 3.9+ (se recomienda 3.10 o 3.11)

**Instalación (entorno virtual recomendado)**
1. Crear y activar un entorno virtual (zsh / bash):

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Instalar dependencias:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

**Ejecución reproducible (pasos recomendados)**
1. Coloca los datasets crudos en `data/raw/` (`posts.csv`, `comments.csv` o sus .jsonl equivalentes).
2. Enriquecer con VADER y agregar métricas por post (genera `data/enriched/`):

```bash
# abrir un editor de código
# luego ejecutar cells en `src/preprocessing.ipynb` en orden
```

3. Preprocesamiento (detección de idioma, limpieza, exportar `data/processed/`):

```bash
# ejecutar `src/preprocessing.ipynb` (Stage 2) o correr las celdas relevantes
```

4. Baseline y modelos:

```bash
# Ejecutar `src/baseline.ipynb` para pipeline TF-IDF + SVM
# Ejecutar `src/model.ipynb` para RandomForest / Logistic / LinearSVC
```