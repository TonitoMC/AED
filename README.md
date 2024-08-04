# Hoja de Trabajo 5. Java Collection Framework / Maps
## Autor: Jose Merida | 4 de Abril 2024
### Instrucciones:
Utilice el de diseño Factory para seleccionar la implementación de MAP que usará su programa, en tiempo de corrida. El
usuario debe seleccionar entre: 1)HashMap, 2)TreeMap, 3)LinkedHashMap.

El programa lee un archivo que contiene una lista de nombres de cartas y si dicha carta es monstruo, trampa o hechizo.
Dichas cartas se agregan a un Mapa que contiene todas las cartas disponibles.

El archivo sigue la siguiente estructura: Cada carta se encuentra en una línea distinta y tiene el nombre luego el carácter | y el
tipo de la carta. Un ejemplo del archivo es el siguiente:
```
Carta 1|Tipo
Nombre de Carta 2|Tipo
...
```
Luego de leer el archivo su programa debe permitir al usuario realizar las siguientes operaciones:
1. Agregar una carta a la colección del usuario. Para esto el usuario ingresa el nombre de la carta que desea agregar a
la misma. NOTA: El usuario puede tener más de una carta de cada tipo. NOTA: Si el usuario ingresa una car ta que
no se encuentra entre las cartas disponibles el programa debe mostrar un error.
2. Mostrar el tipo de una carta específica. El usuario ingresará el nombre de la carta y se muestra el tipo de esa carta.
3. Mostrar el nombre, tipo y cantidad de cada carta que el usuario tiene en su colección.
4. Mostrar el nombre, tipo y cantidad de cada carta que el usuario tiene en su colección, ordenadas por tipo.
5. Mostrar el nombre y tipo de todas las cartas existentes.
6. Mostrar el nombre y tipo de todas las cartas existentes, ordenadas por tipo.

### Tiempo de Corrida Total para cada Implementación
Se utilizío el método showAvailable() para mostrar todas las cartas disponibles y se midió el tiempo de corrida

HashMap

![image](https://github.com/user-attachments/assets/64e6f451-31f2-48f0-96e0-faef540b7177)

TreeMap

![image](https://github.com/user-attachments/assets/c05e2c95-cc07-4cf3-ae2a-3ff947507de6)

LinkedHashMap

![image](https://github.com/user-attachments/assets/2340af0d-f7a8-40d0-bdc1-4933f082799b)
