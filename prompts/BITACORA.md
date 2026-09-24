# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (GEMINI)

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |7|34|
| The students program in Java. |6|29|
| desafortunadamente |4|18|

En el paso 4 si llego a responder bien porque sabia el contexto

En el paso 5 no llego a responder biern porque no tiene el contexto que se utilizo en el paso 4

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 |100%|BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec|
| 0.5 |65.3%|BiblioTec, LibroYa, BiblioTec, BiblioTec, LibroYa|
| 1 |44.5%|LibroYa, BiblioTec, BiblioTec, BiblioTec, LibroYa|
| 1.8 |32.2%|LibroYa, NubeDeTinta, BiblioTec, LibroYa, LibroYa|


## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |SI|SI|
| Menciona a los usuarios principales |NO|SI|
| Tiene exactamente 3 funcionalidades |NO|SI|
| Esta en 3 parrafos |NO|SI|
| Lo usaria en un informe real |NO|SI|

 
## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Crea un programa en Java.|
| Instruccion |Actua como desarrollador Java. Crea un programa en Java.|
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.|
| Ejemplo |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.usando una clase Producto con los atributos codigo, nombre, precio y stock.|
| Formato |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.usando una clase Producto con los atributos codigo, nombre, precio y stock Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).|

Nivel 1:La IA eligió libremente un tema al azar (creó un Main) al no tener restricciones ni contexto especificado.
Nivel 2 (+Rol):Al asumir el rol de desarrollador Java, mejoró la calidad técnica del código usando colecciones dinámicas (ArrayList), dividiendo el código en métodos y agregando una explicación final de las funciones de lo que hacia ciertas partes del codigo.
Nivel 3 (+Contexto):Al agregar el contexto ("para gestionar los productos de una tienda"), enfocó todo el dominio del programa en un inventario comercial, definiendo una clase Producto genérica y operaciones de tienda y explocando para que sirven cada parte de las clases.
Nivel 4 (+Instrucción):Al añadir la instrucción detallada sobre la clase Producto, reemplazó el atributo genérico del nivel anterior por codigo, creó el constructor correspondiente y definio sus métodos getters.
Nivel 5 (+Formato +Ejemplo):Al especificar el formato ("Explica primero los atributos privados"), e incluyó un resumen final de lo que hacia cada clase.
 
## Ejercicio 6: Del prompt basico al profesional

| Qué revisar | Cumple (Sí / No) |
|------------|--------------------|
| ¿Está escrito en Java y usa Swing? |SI|
| ¿Pide correo y contraseña? |SI|
| ¿Explica el funcionamiento antes o después del código? |SI|
| ¿El código está organizado en clases? |SI|
| ¿Valida los datos que ingresa el usuario? |SI|

```text
("Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases." y "Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.")
```