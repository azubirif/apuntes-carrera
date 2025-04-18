---
title: Lenguaje C
---

# Variables
## Tipos de variables

| Tipo       | Espacio | Explicación                        | Tipo en `printf`                                   |
| ---------- | ------- | ---------------------------------- | -------------------------------------------------- |
| `int`      | 4 bytes | Números enteros                    | `%d`                                               |
| `short`    | 2 bytes | Enteros pequeños                   | `%d`                                               |
| `long`     | 8 bytes | Enteros grandes                    | `%ld`                                              |
| `unsigned` |         | Solo para números positivos        |                                                    |
| `float`    | 4 bytes | Números decimales                  | `%f`. `%.decimalesf` para obtener tantos decimales |
| `double`   | 8 bytes | Igual que `float` pero más espacio | `%f`                                               |
| `char`     | 1 bytes | Caracteres                         | `%c`                                               |
| `char[]`   |         | Cadena de caracteres               | `%s`                                               |

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
## Constantes
Se definen antes de los `include`.
```
#define VARIABLE VALOR
```
Las constantes se escriben en mayúsculas (por convención).
# Entrada y salida
Para imprimir por pantalla utilizaremos `printf`
```
printf("Texto a escribir", variables...);
//Ejemplo
printf("Soy %s y tengo %d años", "Alejandro", 19);
```
Para leer información, utilizaremos `scanf`
```
scanf("tipo de la variable", &nombre_variable);
```
Esto no es necesario para cadenas de caracteres, ya que por sí mismos son punteros.
# Casting
Existen dos formas:
- **Implícito**: el compilados se encarga de intentar deducir el resultado final:
```
int i = 9 / 2; //Devuelve 4
int i = 9.0 / 2; //Devuelve error porque creamos un entero y le asignamos un float
```
- **Explícito**: nos encargamos de definir el tipo por nuestra cuenta:
```
int i = (int)9/2; //Devuelve 4
float j = (float) 9/2; //Devuelve 4.5
```
# Punteros
Para obtener la dirección en la memoria de una variable, utilizamos
```
&nombre_variable
```
Para obtener el contenido de un puntero
```
*puntero
```
# Operadores

| Operador | Símbolo |
| -------- | ------- |
| `NOT`    | `!`     |
| `AND`    | `&&`    |
| `OR`     | `\|\|`  |
# Condicionales
La instrucción `if` comprueba si se cumple la expresión lógica (condición) devuelve `True`:
```
if (condición)
{
	//
}
else if
{
	//
}
else
{
	//
}
```
# Bucles
Definimos los bucles mediante un valor inicial, una condición, y un incremento:
```
for (init; condition; increment)
{
	//
}

for (int i = 0; i < 10; i++)
{
	//
}
```
Para hacer un bucle infinito con `for`, podemos hacer
```
for ( ; ; )
{
	//
}
```
Lo más común es el `while`:
```
while (condition)
{
	//
}
```
# Funciones
Una función es un bloque de código que permite reutilizar código que se vaya a utilizar muchas veces.
```
type nombre(args...)
{
	//

	return <type>;
}
```
Podemos distinguir dos formas de pasar argumentos:
- **Paso por valor**: `void incrementar(int x)`
- **Paso por referencia**: `void incrementar(int *x)`
**Ejemplo**:
```
#include <stdio.h>

void inc(int *n)
{
    *n += 1;
}

int main()
{
    int a = 0;
    
    printf("%d\n", a); //0
    
    inc(&a);
    
    printf("%d\n", a); //1
    
    return 0;
}
```
Podemos acceder a elementos específicos de un array de la siguiente forma:
```
#include <stdio.h>

int main()
{
    int a[2];
    *a = 5; //Asignamos el primer elemento del array a 5
    
    int *p = a + 1; //Un puntero que apunta al segundo elemento
    
    *p = 10; //Definimos el segundo elemento como 10
    
    for (int i = 0; i < 2; i++)
    {
        printf("%d\n", *(a+i));
    }
    //5
    //10
}
```
