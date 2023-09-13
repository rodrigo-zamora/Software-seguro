# Common Weakness Enumeration vs CERT coding standards

## Common Weakness Enumeration

**Common Weakness Enumeration** (CWE) es un sistema de categorías para las debilidades y vulnerabilidades del software. Se sustenta en un proyecto comunitario con el objetivo de comprender las fallas en el software y crear herramientas automatizadas que se puedan utilizar para identificar, corregir y prevenir esas fallas.​ El proyecto está patrocinado por National Cybersecurity FFRDC, que es operado por [The MITRE Corporation](https://es.wikipedia.org/wiki/The_MITRE_Corporation), con el apoyo de US-CERT y la División Nacional de Seguridad Cibernética del Departamento de Seguridad Nacional de Estados Unidos.

## CERT coding standards

Los Estándares de Codificación CERT del SEI son estándares de codificación de software desarrollados por el **Centro de Coordinación CERT** para mejorar la seguridad, fiabilidad y protección de los sistemas de software. Se ofrecen estándares individuales para C, C++, Java, Android OS y Perl.

### Ejemplos

#### Ejemplo 1: [ERR34-C. Detect errors when converting a string to a number](https://wiki.sei.cmu.edu/confluence/display/c/ERR34-C.+Detect+errors+when+converting+a+string+to+a+number)

En este código, se cumple con el estándar ERR34-C del CERT al utilizar `sscanf` para intentar convertir una cadena en un número entero. Además, se verifica si la conversión fue exitosa mediante la comprobación del valor devuelto por `sscanf`. Si la conversión falla, se maneja el error adecuadamente.

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    char input[] = "123abc";
    int number;

    // Convertir la cadena en un número
    if (sscanf(input, "%d", &number) == 1) {
        printf("Número convertido: %d\n", number);
    } else {
        printf("No se pudo convertir la cadena en un número.\n");
    }

    return 0;
}
```

#### Ejemplo 2: [NUM09-J. Do not use floating-point variables as loop counters](https://wiki.sei.cmu.edu/confluence/display/java/NUM09-J.+Do+not+use+floating-point+variables+as+loop+counters)

En este código, se cumple con el estándar NUM09-J del CERT al utilizar una variable entera `numIterations` como contador de bucle en lugar de una variable de punto flotante, lo que mejora la precisión en operaciones de bucle. Gracias por la corrección.

```java
public class LoopCounterExample {
    public static void main(String[] args) {
        int numIterations = 10;
        double total = 0.0;

        for (int i = 0; i < numIterations; i++) {
            total += 0.1; // Utilizando un valor decimal en lugar de un bucle con punto flotante
        }

        System.out.println("Total: " + total);
    }
}

```

#### Ejemplo 3: [STR30-C. Do not attempt to modify string literals](https://wiki.sei.cmu.edu/confluence/display/c/STR30-C.+Do+not+attempt+to+modify+string+literals)

En este código, se viola el estándar STR30-C del CERT al intentar copiar un literal de cadena en `dest` utilizando `strcpy`, lo que no está permitido ya que los literales de cadena son de solo lectura y no deben modificarse. Gracias por la corrección.

```c++
#include <iostream>
#include <cstring>

int main() {
    char source[] = "Hello, world";
    char dest[5];

    // Intentar copiar un literal de cadena en dest
    strcpy(dest, "Hello"); // Esto viola STR30-C

    std::cout << "Dest: " << dest << std::endl;

    return 0;
}
```

## Similitudes

- **Enfoque en la seguridad de software:** Tanto CWE como CERT Secure Coding Standards se centran en abordar y prevenir debilidades comunes en el software que pueden ser explotadas por atacantes.

- **Clasificación de vulnerabilidades:** Ambos proporcionan una clasificación detallada de diferentes tipos de debilidades y vulnerabilidades en el software, lo que facilita la identificación y corrección de problemas específicos.

- **Orientados a mejores prácticas:** Los dos se basan en buenas prácticas de programación y diseño seguro de software para ayudar a los desarrolladores a escribir código más seguro y resistente a ataques.