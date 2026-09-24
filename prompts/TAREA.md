# Tarea: Mi prompt profesional

## Funcionalidad elegida

Un Sistema de Registro de Mascotas para una Veterinaria.

## Version 1: prompt basico

```text

Hazme un codigo para Un Sistema de Registro de Mascotas para una Veterinaria.

Qué cambiaste: Se inició con la idea principal del proyecto sin especificar lenguaje ni arquitectura.

Por qué: Para observar la respuesta por defecto del modelo ante una instrucción vaga.

Qué mejoró en la respuesta: La IA generó un código funcional básico en Python usando POO, pero no estaba adaptado al entorno de trabajo deseado (Java / Eclipse).

```

## Version 2

```text

Hazme un codigo para Un Sistema de Registro de Mascotas para una Veterinaria. para java que sea compatible con eclipe

Qué cambiaste: Se especificó el lenguaje de programación (Java) y el entorno de desarrollo (Eclipse IDE).

Por qué: Se requería que el código generado se pudiera ejecutar directamente en la herramienta utilizada en clase.

Qué mejoró en la respuesta: La IA cambió el lenguaje de Python a Java y añadió explicaciones paso a paso de cómo crear el proyecto en Eclipse. Sin embargo, la estructura interna del código aún no definía los campos requeridos.

 ```

## Version 3: prompt final

```text

Actua como desarrollador Java experto. Crea un Sistema de Registro de Mascotas para una Veterinaria. El usuario debe ingresar nombre del dueño y de la mascota y numero de fila de la mascota . Explica brevemente el funcionamiento y presenta el codigo organizado por clases. y que sea compatible con eclipse no uses librerias externas

Qué cambiaste: Se asignó un Rol (desarrollador Java experto), campos de datos específicos (dueño, mascota, número de fila), formato de salida (organizado por clases y breve explicación) y compatibilidad con Eclipse.

Por qué: Para obtener un código modular, mantenible y ajustado exactamente a los requerimientos del dominio.

Qué mejoró en la respuesta: La respuesta fue altamente estructurada, proporcionando clases independientes en Java, explicaciones de la arquitectura modular y compatibilidad garantizada con Eclipse.

```

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Actua como desarrollador Java experto.|
| Instruccion |Crea un Sistema de Registro de Mascotas para una Veterinaria... Explica brevemente el funcionamiento y presenta el codigo...|
| Contexto |El usuario debe ingresar nombre del dueño y de la mascota y numero de fila de la mascota... y que sea compatible con eclipse|
| Ejemplo |Actua como desarrollador Java experto. Crea un Sistema de Registro de Mascotas para una Veterinaria El usuario debe ingresar nombre del dueño y de la mascotra y numero de fila de la mascota .|
| Formato |Actua como desarrollador Java experto. Crea un Sistema de Registro de Mascotas para una Veterinaria El usuario debe ingresar nombre del dueño y de la mascotra y numero de fila de la mascota .|
|Restricción|No importar librerias externas|
 
## Evaluacion del resultado
 
 | Qué revisar | Cumple (Sí / No) |
|------------|--------------------|
| ¿El código genera las clases necesarias en Java? |SI|
|  ¿Incluye los campos especificados (dueño, mascota, número de fila)?|SI|
| ¿Es directamente ejecutable en Eclipse IDE? |SI|
| ¿Explica brevemente el funcionamiento del sistema? |SI|

## Errores que evite

1.-Ser demasiado general: En la v1 solo pedí "un sistema de registro", lo que provocó que la IA eligiera un lenguaje al azar (Python). Lo evité en la v3 especificando exactamente el rol, el lenguaje y las clases requeridas.

2.-No dar contexto ni indicar el formato: En las primeras versiones no definí la entrada de datos ni la organización del código. En el prompt final detallé los atributos requeridos (dueño, mascota, número de fila) y pedí explícitamente que el código estuviera estructurado por clases.