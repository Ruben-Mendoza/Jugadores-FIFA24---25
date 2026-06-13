# FIFA Players Position Classification Datasets (2024 & 2025)

> Proyecto final — **Ciencia de Datos**  
> Licenciatura en Matemática Aplicada · FAMAF, Universidad Nacional de Córdoba  

---

## Descripción

Aplicación de modelos de clasificación supervisada para **predecir la posición en el campo de juego** de jugadores de fútbol a partir de sus atributos numéricos (valoraciones de habilidades del estilo FIFA).

## Descripción del conjunto de datos

Este repositorio contiene tres conjuntos de datos procesados derivados de jugadores de FIFA de los años 2024 y 2025, diseñados para entrenar y evaluar modelos de clasificación de posiciones de fútbol:

1. **`df_fifa_24`**:  
   - Datos de jugadores de FIFA 2024.  
   - Contiene solo las columnas presentes en ambos años (2024 y 2025) para garantizar compatibilidad.  
   - Cada jugador tiene una única posición asignada en la columna `Position` (etiqueta de clasificación).

2. **`df_fifa_25`**:  
   - Datos de jugadores de FIFA 2025, filtrados para incluir **solo jugadores nuevos que no aparecen en el dataset de 2024**.  
   - Mantiene las mismas columnas que `df_fifa_24`.  
   - Ideal para probar modelos entrenados con datos de 2024 en jugadores "no vistos".

3. **`df_fifa_24_multi`**:  
   - Subconjunto especial de jugadores de FIFA 2024 que tienen **múltiples posiciones** asignadas en la columna `Position`.  
   - Útil para evaluar la capacidad de los modelos de clasificar jugadores "híbridos" en sus posiciones más probables.

### Modelos comparados

Naive Bayes · LDA · Regresión Logística · Perceptrón · K-Nearest Neighbors · Random Forest

### Sets de datos comparados

- Datos completos
- Datos reducidos por correlación
- Datos reducidos por PCA

### Métrica principal

Se define una métrica personalizada de **Precisión Mediocampista** para penalizar específicamente las confusiones entre mediocampistas, defensores y delanteros, que son las posiciones con mayor solapamiento de atributos.

---

## Metodología

- **Validación cruzada estratificada** con 9 folds para evaluación robusta de todos los modelos.
- **Búsqueda de hiperparámetros** para cada modelo sobre cada set de datos.
- **Proyección LDA** de los datos de FIFA 2025 para visualización de la separabilidad entre posiciones.

---

## Tecnologías y herramientas

- **Lenguaje:** Python 3
- **Bibliotecas:** `scikit-learn`, `numpy`, `pandas`, `matplotlib`, `seaborn`
- **Documentación:** LaTeX (Beamer)

---

## Conclusiones

Los modelos entrenados con los **datos completos** presentaron el mejor rendimiento, superando a las versiones reducidas por PCA o correlación. Los atributos de los jugadores permiten diferenciar posiciones con buen desempeño predictivo y capacidad de generalización a temporadas futuras (2025).

**Aplicación práctica:** el modelo entrenado puede usarse para sugerir la posición óptima a jugadores con múltiples roles asignados, facilitando decisiones tácticas.

---
