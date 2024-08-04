# Hoja de Trabajo 9: Grafos y Dijkstra
### Autores: José Antonio Mérida Castejón y Adrián López | 12 de Mayo 2024
Este programa implementa un sistema para agendar viajes, lee datos de un archivo llamado "rutas.txt" que contiene la estación de salida, el destino y el costo.

El archivo "rutas.txt" sigue el siguiente formato:
```
"Pueblo Paleta", "Aldea Azalea", 100
"Aldea Azalea", "Ciudad Safiro", 150
"Pueblo Paleta", "Ciudad Safiro", 800
"Ciudad Lavanda", "Aldea Fuego", 300
```
Al iniciar el programa se despliega un grafo que muestra las rutas del archivo, al igual que el costo entre cada salida y destino. 

![image](https://github.com/user-attachments/assets/7b976987-f298-4f7f-90f3-af4b4951ecb5)



Luego se le pide al usuario ingresar el nombre de la estación de salida, se utiliza el algoritmo de Dijkstra para determinar las rutas más cortas para cada destino posible. En el caso de elegir como estación de salida "Pueblo Paleta" se obtiene el siguiente output:
```
Destino: Aldea Azalea, Ruta: Pueblo Paleta -> Aldea Azalea, Distancia: 100
Destino: Ciudad Safiro, Ruta: Pueblo Paleta -> Aldea Azalea -> Ciudad Safiro, Distancia: 250
```
Adicionalmente se genera el siguiente Grafo:

![image](https://github.com/user-attachments/assets/f40d7e8e-8f1b-4f5a-bc91-e8a41a59eeac)

También incluye la funcionalidad de re-dibujar los grafos, en caso que el Seed del Spring Layout cree un overlap entre diferentes nodos o la imagen no esté lo suficientemente clara. Se evito utilizar posicionamiento individual de cada grafo ya que pueden tener un número variable de Nodos y conexiones entre ellos, los parámetros del Spring Layout fueron probados empíricamente y se buscó el resultado más consistente.
## Instalación
Este proyecto fue escrito en [Python](https://www.python.org/). Utiliza [NetworkX](https://networkx.org/), [Numpy](https://numpy.org/) y [Matplotlib](https://matplotlib.org/), por lo cuál es necesario tener instaladas estas dependencias para asegurar el funcionamiento correcto del programa.
