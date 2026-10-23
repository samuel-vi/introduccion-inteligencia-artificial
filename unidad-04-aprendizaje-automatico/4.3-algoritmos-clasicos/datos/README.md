# Datos de las prácticas

## Consumo sintético
180 observaciones independientes simuladas, semilla 43. Objetivo hipotético en kWh: `2 + 1.8*horas + 4*carga + 0.12*temperatura + ruido`, con ruido normal de desviación 0.9. No son mediciones de equipos reales. La fórmula generadora pertenece a la explicación docente; el alumnado ajusta el modelo con entrenamiento.

## Wine
Conjunto real Wine incluido con scikit-learn: 178 ejemplos, 13 características y tres clases de cultivares. Origen: UCI Machine Learning Repository, Wine, donantes M. Forina et al.; autores de referencia S. Aeberhard et al. Consulte `wine-descripcion.txt` y https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html . Las variables son análisis químicos y la etiqueta identifica el cultivar, no calidad, seguridad ni un diagnóstico clínico.

## Particiones
Cada CSV incluye una columna `particion` que NO es una entrada. Distribución aproximada 60/20/20, semilla 43; estratificación por clase en Wine. Se conserva la misma partición para todos los clasificadores. Los notebooks 01–03 utilizan entrenamiento y validación; el 04 consulta prueba solo después de seleccionar. No modificar particiones para mejorar resultados.

