# Maximizacion Cubica con Algoritmos Geneticos

Proyecto de trabajo para los ejercicios de Algoritmos Geneticos, enfocado en maximizar la funcion $f(x) = x^3 - 4x^2 + 5x$ con una implementacion didactica en Python.

## Autor y tutor

| Rol | Nombre |
|---|---|
| Autor 1  | Jorge Nicolas Castro Ballesteros - jncastro@ucundinamarca.edu.co |
| Autor 2  | Juana Valentina Espitia Gomez - jvespitia@ucundinamarca.edu.co |
| Tutor | Fabio Alejandro Sastoque Rincon |
| Universidad | Universidad de Cundinamarca - Seccional Ubate |

## Proyecto

- [max_cubica.ipynb](max_cubica.ipynb): notebook principal con el algoritmo genetico, la decodificacion binaria y las graficas de convergencia (Ejercicio 1 - Maximizacion cubica).
- [clase_1_ag.py](clase_1_ag.py): archivo de referencia para la estructura general del algoritmo.
- [Dataset/Ice_cream selling data.csv](Dataset/Ice_cream%20selling%20data.csv): dataset de contexto visual usado en las graficas finales. Aplicado en Ejercicio 1 y 3.

## Ejercicios

### Ejercicio 1 - Maximizacion cubica
Adapta la funcion de aptitud para maximizar f(x) = x^3 - 4x^2 + 5x en un rango donde la funcion tiene un maximo local claro. Ver `max_cubica.ipynb`.

### Ejercicio 2 - Optimizacion multivariable
El cromosoma binario se divide en dos mitades (4 bits para x, 4 bits para y), cada una decodificada al rango [-5, 5]. Minimiza f(x, y) = x^2 + y^2 usando -f(x, y) como aptitud. Converge cerca del optimo teorico (0, 0). Ver `Ejercicio_2_Multivariable.ipynb`.

### Ejercicio 3 - Impacto de la tasa de mutacion
Ejecuta el algoritmo del Ejercicio 1 con tres probabilidades de mutacion distintas (pm = 0.01, 0.1 y 0.5) y compara las graficas de convergencia resultantes. `tasa_mutacion.ipynb`.

### Ejercicio 4 - Elitismo ampliado
Modifica la funcion de elitismo para preservar de forma intacta a los 3 mejores individuos de cada generacion (n_elite=3), en lugar de solo 1. Incluye una comparacion de convergencia entre elitismo estandar (n=1) y ampliado (n=3) con la misma semilla. Ver `Ejercicio_4_Elitismo.ipynb`.

## Tecnologias

Tecnologia y entorno

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![NumPy](assets/badges/numpy.svg)
![Pandas](assets/badges/pandas.svg)
![Matplotlib](assets/badges/matplotlib.svg)
![ipywidgets](assets/badges/ipywidgets.svg)
![Jupyter](assets/badges/jupyter.svg)
![Licencia](https://img.shields.io/badge/Licencia-MIT-4CAF50)

## Configuracion del entorno

1. Clona el repositorio:
   ```
   git clone https://github.com/RavenCore99/ML_Algoritmos-_Geneticos.git
   cd ML_Algoritmos-_Geneticos
   ```

2. Crea y activa el entorno virtual:

   **Windows (PowerShell):**
   ```
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```

   **macOS / Linux:**
   ```
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Instala las dependencias:
   ```
   pip install jupyter matplotlib numpy pandas ipywidgets
   ```

4. Abre los notebooks en Visual Studio Code (extension de Jupyter) o con:
   ```
   jupyter notebook
   ```

## Flujo de trabajo en Git

- Cada integrante trabaja en su propia rama (`feature/nombre-ejercicio`), nunca directamente en `AG` (rama principal del proyecto).
- Los cambios se suben mediante `git push origin <rama>` y se integran a `AG` a traves de un Pull Request.
- La carpeta `.venv` y archivos temporales estan excluidos mediante `.gitignore`.

## Como ejecutar cada notebook

1. Abre el archivo `.ipynb` correspondiente en VS Code.
2. Selecciona el kernel del entorno virtual (`.venv`).
3. Ejecuta todas las celdas en orden (`Run All`).
4. Revisa las graficas de convergencia generadas al final de cada notebook.
