# Práctica: Manejo de Excepciones y Errores en Python

## Introducción:

El manejo de excepciones y errores es una parte esencial en el desarrollo de software. Permite que un programa responda de manera controlada cuando se producen situaciones inesperadas. En Python, las excepciones se gestionan mediante bloques .[`try`, `except`, `else` y `finally`.](documentacion.md) 

## Objetivos:

1. Comprender el concepto de excepciones y cómo se manejan en Python.
2. Aprender a utilizar bloques `try`, `except`, `else` y `finally`.
3. Practicar el manejo de excepciones para mejorar la robustez del código.

## Teoría:

### Excepciones en Python:

En Python, una excepción es un evento que ocurre durante la ejecución de un programa y afecta el flujo normal de ejecución. Algunas excepciones comunes incluyen `ZeroDivisionError`, `TypeError`, `FileNotFoundError`, entre otras.

### Manejo Básico de Excepciones:

```python
try:
    # Código susceptible de generar una excepción
    resultado = 10 / 0
except ZeroDivisionError:
    # Manejo de la excepción específica
    print("¡Error! División por cero.")
except Exception as e:
    # Manejo de excepciones generales
    print(f"¡Error general: {e}!")
else:
    # Bloque ejecutado si no se produce ninguna excepción
    print("La operación se realizó con éxito.")
finally:
    # Bloque que se ejecuta siempre, haya o no excepción
    print("Fin del bloque try.")
```

### Personalizando Excepciones:

```python
class MiErrorPersonalizado(Exception):
    def __init__(self, mensaje="Ha ocurrido un error personalizado."):
        self.mensaje = mensaje
        super().__init__(self.mensaje)

try:
    raise MiErrorPersonalizado("Este es un mensaje personalizado.")
except MiErrorPersonalizado as e:
    print(f"¡Error personalizado: {e}!")
```

## Práctica:

### Ejercicio 1: Manejo de Excepciones Básico

Escribe un programa que solicite al usuario dos números y realice la división. Implementa el manejo de excepciones para evitar errores de división por cero y asegurarte de que el usuario ingrese números válidos.

### Ejercicio 2: Personalización de Excepciones

Crea una clase de excepción llamada `EdadInvalidaError` que se levante si un usuario intenta ingresar una edad negativa. Modifica el programa para que utilice esta excepción al solicitar la edad de una persona.

### Ejercicio 3: Manejo de Errores en Archivos

Crea un programa que intente abrir un archivo especificado por el usuario. Implementa el manejo de excepciones para capturar posibles errores, como la no existencia del archivo.

## Conclusiones:

Reflexiona sobre la importancia del manejo de excepciones para mejorar la estabilidad y robustez de un programa. Considera cómo el uso adecuado de bloques `try`, `except`, `else` y `finally` puede facilitar la identificación y resolución de problemas en el código.

[Consulte la rúbrica de evaluación antes subir su práctica](rubrica.md) 