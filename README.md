# FIFA Players Position Classification Datasets (2024 & 2025)

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
