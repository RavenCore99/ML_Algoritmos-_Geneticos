# Ejercicio 4 - Elitismo ampliado

**Integrante:** (tu nombre)

## Descripción

Se modifica la función interna de elitismo del algoritmo genético para que, en lugar de preservar solo al mejor individuo (elitismo estándar, n=1), preserve de forma intacta a los 3 mejores individuos de cada generación (n_elite=3) hacia la siguiente.

## Función objetivo

Se reutiliza la función de aptitud del Ejercicio 1: f(x) = x³ - 4x² + 5x, maximizada en el rango x ∈ [0, 1.8].

## Comparación incluida

El notebook incluye una comparación de convergencia entre elitismo n=1 y n=3 usando la misma semilla aleatoria, como evidencia del efecto del cambio.

## Resultado

Ambas configuraciones convergen al óptimo (x=1, f(x)=2), con diferencias en la velocidad de convergencia inicial.

## Archivo

`Ejercicio_4_Elitismo.ipynb`
