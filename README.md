# Proyecto 1: Intérprete LISP en Java
## Autores: José Antonio Mérida, Adrián López
Este proyecto implementa un sistema de recomendaciones de videojuegos utilizando una base de datos basada en grafos. La base de datos fue creada utilizando el servicio de [AuraDB](https://neo4j.com/cloud/platform/aura-graph-database/) y datos recopilados sobre los juegos de la plataforma [Steam](https://store.steampowered.com/) obtenidos de [Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset).
## Instalación
Este proyecto utiliza [Maven](https://maven.apache.org/) y fue escrito en [Java](https://www.java.com/en/), por lo cual es necesario instalar estas dependencias para poder correr el programa. Para proteger los datos de los usuarios y el acceso a la base de datos, la información de conexión se coordina por medio de variables de entorno, por lo cuál es necesario configurarlas para conectarse a la base de datos de AuraDB con los datos cargados.
## Instrucciones
Desarrollo de un intérprete LISP para un subconjunto sencillo de instrucciones de alguno de los dos
dialectos principales (Common LISP y Scheme). Deben implementarse como mínimo:

a) operaciones aritméticas,

b) instrucción QUOTE o ‘ (single quote, para interrumpir el proceso de evaluación de expresiones)

c) definición de funciones (DEFUN)

d) SETQ

e) predicados (ATOM, LIST, EQUAL, <, >)

f) condicionales (COND), nota: no es necesario implementar IF

g) paso de parámetros. (un parámetro puede ser incluso una función)

NOTA: recuerde que LISP es un lenguaje que permite recursividad, por lo que sus funciones deben
soportarlo.

El intérprete desarrollado deberá permitir ejecutar programas sencillos en LISP.

## Video Demostrativo
[Link](https://youtu.be/iEC88OQhkGQ)

## Programa por Correr
```
(print (+ 3 7))
(print (* 2 (- 7 4) 7))
(SETQ variable1 10)
(print variable1)
(print (QUOTE variable1))

(defun orden (num1 num2 num3)
(COND
((< num1 num2 num3) (print "Ascendente"))
((> num1 num2 num3) (print "Descendiente"))
((= num1 num2 num3) (print "Iguales"))
(t (print "Ninguno"))))

(orden 1 2 3)
(orden 3 2 1)
(orden 1 1 1)
(orden 2 1 3)

(SETQ variable8 (list 1 2 3))

(print(ATOM variable8))
(print(ATOM variable1))

(defun sumartresnumeros (num1 num2 num3)
(+ num1 num2 num3))

(print (sumartresnumeros 1 2 3))
(print (sumartresnumeros (sumartresnumeros 1 2 3) 2 3))

(defun factorial (n)
  (COND ((= n 0) 1)
        ((= n 1) 1)
        (t (* n (factorial (- n 1))))))

(print (factorial 5))
```
Output:
```
10.0
42.0
10
variable1
"Ascendente"
"Descendiente"
"Iguales"
"Ninguno"
false
true
6.0
11.0
120.0
```

## Diseño del Intérprete
### Diagrama de Clases
![image](https://github.com/user-attachments/assets/8996f88a-ad31-45bb-9764-e2aa46577d49)

### Diagrama de Estados
![image](https://github.com/user-attachments/assets/c19018e1-a32d-4459-924a-7aea3edbcead)

### Diagrama de Secuencias
![image](https://github.com/user-attachments/assets/be0f44dc-aff5-4054-9c0e-22d26439b3ec)
