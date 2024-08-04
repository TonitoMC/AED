# Hoja de Trabajo 5. Simulacion CPU
## Autor: Jose Merida | 4 de Marzo 2024
### Instrucciones:
Simulación de corrida de programas en un sistema operativo de tiempo compartido (el procesador se comparte por una
porción de tiempo entre cada programa que se desea correr). En la terminología de sistemas operativos se llama “proceso” a
un programa que se ejecuta. La siguiente figura muestra el ciclo de vida de un proceso dentro del sistema operativo

![image](https://github.com/user-attachments/assets/33f611a9-d5cb-44db-8450-1700dda0e719)

**new:** el proceso llega al sistema operativo pero debe esperar que se le asigne memoria RAM. En nuestra simulación el
proceso solicitará una cantidad de memoria (número entero al azar entre 1 y 10). Si hay memoria disponible puede pasar al
estado de ready. En caso contrario permanece haciendo cola, esperando por memoria. NOTA: la cantidad de memoria
disponible se disminuye con la cantidad de memoria que empleará el proceso que logró obtenerla.

**ready:** el proceso está listo para correr pero debe esperar que lo atienda el CPU. El proceso tiene un contador con la cantidad
de instrucciones totales a realizar (número entero al azar entre 1 y 10). Cuando se desocupa el CPU puede pasar a utilizarlo.

**running:** el CPU atiende al proceso por un tiempo limitado, suficiente para realizar solamente 3 instrucciones (esto será
configurado, ya que podrá crecer o reducirse). Al completarse el tiempo de atención el proceso es retirado del CPU. Se debe
actualizar el contador de instrucciones a realizar, disminuyendo las 3 instrucciones que ejecutó en esta oportunidad. Si el
proceso tiene menos de tres instrucciones que le hace falta procesar, libera el CPU anticipadamente.

Al finalizar la atención del CPU puede ocurrir:

a)Terminated: Si el proceso ya no tiene instrucciones por realizar entonces pasa al estado “terminated” y sale del sistema.

b)Waiting: al dejar el CPU se genera un número entero al azar entre 1 y 21. Si es 1 entonces pasa a la cola de Waiting par a
hacer operaciones de I/O (entrada/salida). Al dejar esa cola regresa a “ready”.

c)Ready: al dejar el CPU y el número generado al azar es 2 entonces se dirige nuevamente a la cola de “ready”.

### Outputs
En el archivo HDT5 AED.pd se encuentran graficas y especificaciones de los datos obtenidos, al igual que un link a un spreadsheet con toda la informacion recopilada.
