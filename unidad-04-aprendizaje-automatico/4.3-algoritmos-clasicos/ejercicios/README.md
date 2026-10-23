# Ejercicios progresivos de 4.3

**Procedencia:** elaboración didáctica para este curso basada en Géron, caps. 2–5, y Grus, caps. 13–16. No son transcripciones de ejercicios del libro. Las cifras son hipotéticas salvo los resultados identificados de Wine. Consulte el apunte antes de resolver y reserve las soluciones para el final.

## Nivel 1 · Formulación y cálculo

### E1. Formular antes de entrenar

Clasifique cada tarea como regresión o clasificación: (a) estimar kWh; (b) predecir tipo de falla codificado 0, 1, 2; (c) anticipar latencia en milisegundos; (d) identificar spam. Para (b) defina entradas, etiqueta y momento de predicción. Explique por qué no puede usar como entrada el resultado de una revisión realizada después de la predicción.

### E2. Ajustar una recta

Utilice x=[1,2,3,4,5] horas e y=[3,4,6,8,9] kWh hipotéticos. Calcule medias, numerador, denominador, pendiente e intercepto. Complete una tabla con predicción y residuo por observación. Compruebe que la suma de residuos es aproximadamente cero al incluir intercepto.

### E3. Medir e interpretar regresión

Con E2 calcule SSE, MAE, RMSE y R². Distinga errores de ajuste y generalización. Prediga para x=6 y explique si es extrapolación. ¿R²≈0.98 permite afirmar «98 % de exactitud» o una relación causal?

### E4. Regresión múltiple

Un modelo hipotético es ŷ=2+1.8h+4c+0.12T, con h en horas, c como fracción de carga de 0 a 1 y T en °C. Calcule la predicción para h=5, c=0.5 y T=25. Si el valor real es 17.5 kWh, calcule el error firmado real−predicción. Interprete el efecto de aumentar h en una hora manteniendo el resto. Explique por qué no debe introducir c=50 si fue entrenado en fracciones.

### E5. Matriz de confusión

Positiva=falla. VN=50, FP=10, FN=5, VP=35. Calcule exactitud, precisión positiva, sensibilidad, especificidad y F1. Interprete cada resultado con su denominador. Si omitir una falla tiene costo alto, ¿qué error necesita atender? ¿Basta con maximizar exactitud?

## Nivel 2 · Decisiones y supuestos

### E6. Probabilidad y clase

Sea z=−3+0.8x y p=1/(1+exp(−z)). Para x=4 calcule p y la clase con umbral 0.5 y 0.6 usando positiva si p≥umbral. ¿Se volvió a entrenar el modelo? ¿La probabilidad garantiza acierto?

### E7. Umbral y costo de errores

Probabilidades estimadas: [.10,.40,.55,.80,.90,.70]. Etiquetas reales: [0,0,1,1,0,1]. Para umbrales .50 y .75 calcule predicciones, matriz y métricas. Indique qué decisión prioriza detección. No asuma que la precisión mejora siempre al subir el umbral.

### E8. Bayes con una característica

P(spam)=.40; P(palabra|spam)=.75; P(palabra|legítimo)=.10. Calcule P(spam|palabra), mostrando el denominador. ¿Qué supuesto adicional introduciría Naive Bayes al combinar varias palabras? No infiera independencia general de la condición naive.

### E9. Suavizado y variante

Hay 4 mensajes spam y 6 legítimos. Una característica binaria está presente en 3 spam y 1 legítimo. Aplique Laplace (k+1)/(n+2), mantenga previas .4 y .6 y calcule posterior dada presencia. Explique por qué esta fórmula binaria no se traslada sin cambios a conteos multinomiales. Elija entre GaussianNB, BernoulliNB y MultinomialNB para: mediciones continuas, presencia/ausencia y conteos de palabras.

### E10. Margen SVM

Con w=(1,0), b=−2 y etiquetas de signo −1/+1: evalúe f(x)=wᵀx+b en (1,5), (3,0) y (2,8). Localice frontera y rectas canónicas de margen f=−1 y f=+1; calcule distancia entre ellas. ¿El signo de f es una probabilidad? Explique el efecto orientador de C y gamma, sin afirmar que valores mayores siempre mejoran resultados.

## Nivel 3 · Auditoría e interpretación experimental

### E11. Encontrar problemas del procedimiento

Un estudiante (a) ajusta StandardScaler con todos los datos antes de separar; (b) elige C según resultados de prueba; (c) compara el F1 de SVM en Wine con el de Naive Bayes en mensajes distintos; (d) usa la columna particion como característica; (e) afirma superioridad general por una diferencia de un error. Identifique el problema de cada paso y proponga una corrección.

### E12. Seleccionar y reportar

Use la tabla de validación de P4. El criterio previo es mayor F1 macro y empate por orden declarado. Seleccione candidato. Interprete la matriz final de prueba [[12,0,0],[0,12,2],[0,0,10]], con filas reales y clases [0,1,2]. Calcule precisión y sensibilidad de clase1 y clase2; explique cuál omite casos y cuál recibe falsas asignaciones. Redacte un párrafo que distinga evidencia de validación, resultado final y límites.

## Entrega

Tabla de cálculos, interpretación y justificación de decisiones. Los ejercicios de nivel1 se resuelven primero a mano; después se verifican con P1–P2. No se exige implementar un optimizador completo ni una SVM desde cero.

