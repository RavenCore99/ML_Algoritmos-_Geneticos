# Maximizacion Cubica con Algoritmos Geneticos

Proyecto de trabajo para los ejercicios de Algoritmos Geneticos, enfocado en maximizar la funcion $f(x) = x^3 - 4x^2 + 5x$ con una implementacion didactica en Python.

## Autor y tutor

| Rol | Nombre |
|---|---|
| Autor | Jorge Nicolas Castro Ballesteros - jncastro@ucundinamarca.edu.co |
| Tutor | Fabio Alejandro Sastoque Rincon |
| Universidad | Universidad de Cundinamarca - Seccional Ubate |

## Proyecto

- [max_cubica.ipynb](max_cubica.ipynb): notebook principal con el algoritmo genetico, la decodificacion binaria y las graficas de convergencia.
- [clase_1_ag.py](clase_1_ag.py): archivo de referencia para la estructura general del algoritmo.
- [Dataset/Ice_cream selling data.csv](Dataset/Ice_cream%20selling%20data.csv): dataset de contexto visual usado en las graficas finales.

## Tecnologias

 Tecnologia y entorno

 ![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white) 
 ![NumPy](assets/badges/numpy.svg) 
 ![Pandas](assets/badges/pandas.svg)
 ![Matplotlib](assets/badges/matplotlib.svg) 
 ![ipywidgets](assets/badges/ipywidgets.svg) 
 ![Jupyter](assets/badges/jupyter.svg)

## Como ejecutar

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install numpy pandas matplotlib ipywidgets ipykernel
```

Luego abre [max_cubica.ipynb](max_cubica.ipynb), selecciona el kernel de `.venv` y ejecuta las celdas en orden.

## Que se hizo en el codigo

En el notebook [max._cubica.ipynb](max._cubica.ipynb) monte el ejercicio 1 de maximizacion cubica. La meta era encontrar el maximo de f(x) = x³ - 4x² + 5x acotando x entre 0.0 y 1.55, que es donde cae el maximo local en x=1 (f(1)=2).

### Funciones que use

- `fitness_cubica(x)`: devuelve la aptitud de cada individuo con la funcion del enunciado.
- `decode_binary_to_real()`: traduce un cromosoma de 16 bits a un valor real dentro del rango.
- `load_context_dataset()`: lee el csv de helados solo para la grafica de contexto, no entra al calculo del AG.
- `plot_generation_snapshot()`: dibuja la curva cubica, la poblacion de una generacion y el panel que elijas (dataset, top5 o resumen).

### Clase AlgoritmoGenetico

La clase queda modular para reutilizarla despues. Corre 60 generaciones con 40 individuos, pc=0.85, pm=0.03, seleccion por ruleta y elitismo activo. Por dentro hace lo de siempre: inicializar poblacion, calcular fitness, elegir padres, cruzar en un punto, mutar bits y conservar el mejor.

Al terminar deja `ag.last_history_frame` (historial generacion a generacion) y `ag.last_summary_frame` (resumen final con mejor x, fitness, pc, pm, etc.).

### Resultado y visualizacion

Al correrlo salio mejor x = 1.000008 y fitness = 2.0 en la generacion 36, bastante cerca del maximo teorico.

La parte interactiva va con ipywidgets: un slider para moverte entre generaciones y botones para cambiar el panel derecho. A la izquierda siempre se ve la curva con los puntos naranjas de la poblacion y la estrella roja del mejor global. El dataset de helados es solo referencia visual, no afecta el algoritmo.

Las capturas de abajo corresponden a esas tablas y paneles cuando corres el notebook completo.

## Capturas

1. Generacion y tabla principal

![tabla Principal](assets/capturas/1_tabla_generacion.png)



2. Top 5 y comparacion


![Comparacion](assets/capturas/2_tablas_top5.png)



3. Resumen final:

![Resumen final](assets/capturas/3_Tabla_resumen.png)

## Notas

- el notebook esta pensado para un flujo simple y claro para entender el tema lo mejor posible
- las figuras finales ayudan a leer la evolucion del AG y el resultado de la busqueda


![Licencia](https://img.shields.io/badge/Licencia-MIT-4CAF50)
