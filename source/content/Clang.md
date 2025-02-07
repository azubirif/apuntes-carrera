---
title: Lenguaje C
---

# Variables
## Tipos de variables

| Tipo       | Espacio | Explicación                        | Tipo en `printf` |
| ---------- | ------- | ---------------------------------- | ---------------- |
| `int`      | 4 bytes | Números enteros                    | `%d`             |
| `short`    | 2 bytes | Enteros pequeños                   | `%d`             |
| `long`     | 8 bytes | Enteros grandes                    | `%d`             |
| `unsigned` |         | Solo para números positivos        |                  |
| `float`    | 4 bytes | Números decimales                  |                  |
| `double`   | 8 bytes | Igual que `float` pero más espacio |                  |
| `char`     | 1 bytes | Caracteres                         | `%c`             |

## Declaración de variables
Para declarar una variable, tenemos que establecer su tipo, su nombre y (opcionalmente) su valor:
```
tipo nombre = valor;
```
Si tratamos de imprimir una variable que no tiene valor, imprimirá lo que haya en esa dirección de memoria.
También podemos directamente declarar variables del mismo tipo:
```
tipo a,b,c;
tipo a=x, b=y, c=z;
```
## Arrays
Son colecciones de elementos del mismo tipo
```
tipo nombre[] = {...};
tipo nombre[tamaño] = {...}; //Esto es redundante
tipo nombre[tamaño];
```
# Funciones
