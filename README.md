# Agente Watchdog

Watchdog es un modelo abstracto y determinista de una red pequeña que simula la defensa de un guardián frente a una infección. La topología de la red y las reglas de propagación definen el escenario en el que se plantea el problema. La infección avanza por las conexiones entre nodos, desde las cámaras hacia el núcleo, y el agente intenta contenerla eligiendo entre aislar, restablecer o esperar, sin dejar caer el servidor ni la subestación. El proyecto expone la red como un problema de búsqueda sobre la clase `Problem` de [AIMA-Python](https://github.com/aimacode/aima-python), lo que facilita comparar algoritmos como BFS, DFS y A\* sobre el mismo estado inicial.

El notebook sigue este orden, que va de la formalización del problema a los algoritmos, el benchmark y la validación, los parámetros de complejidad, la visualización, las simulaciones de BFS, DFS y A\*, la medición de rendimiento y la tabla comparativa.

## Instalación y dependencias

### Descargar el notebook

Descarga el archivo `AgenteWatchdog.ipynb` y guárdalo en una carpeta.

### Clonar la librería AIMA-Python

Desde esa misma carpeta, clona la librería oficial de AIMA. El notebook la busca junto a él:

```bash
git clone --depth 1 https://github.com/aimacode/aima-python.git
```

### Instalar paquetes requeridos

Instala las dependencias necesarias mediante pip:

```bash
pip install pandas matplotlib jupyter
```

Probado con Python 3.14.

## Ejecución

Desde la carpeta de trabajo, abre el notebook y ejecuta todas las celdas en orden (Kernel, Restart & Run All):

```bash
jupyter notebook AgenteWatchdog.ipynb
```

## Verificación

Al ejecutar la celda del benchmark, los pasos, el costo y los nodos expandidos deben coincidir con esta tabla. El tiempo y la memoria varían según el equipo.

| Algoritmo | Pasos | Costo | Expandidos |
| --- | --- | --- | --- |
| BFS | 4 | 21 | 27 |
| DFS | 12 | 73 | 13 |
| A\* | 4 | 20 | 25 |

## Ejemplo de salida

Cada animación termina mostrando el plan encontrado. A la izquierda está la red, y a la derecha el árbol de búsqueda con cada nodo como una mini-red.

### BFS

<img width="1339" height="668" alt="BFS" src="https://github.com/user-attachments/assets/4c90e0c0-a7c7-4bb3-8b8e-9635cc54d7a3" />

### DFS

<img width="1304" height="647" alt="DFS" src="https://github.com/user-attachments/assets/5c3af988-9f39-4e93-b12c-4abd740f9113" />

### A\* con heurística admisible

<img width="1343" height="671" alt="Astar" src="https://github.com/user-attachments/assets/a2c1b7e4-6849-44f7-968e-f93b2458c98f" />

### Comparación de los tres algoritmos

<img width="1590" height="468" alt="Tabla comparativa" src="https://github.com/user-attachments/assets/b3da4851-033f-4b4b-938f-d1bf9c675967" />
