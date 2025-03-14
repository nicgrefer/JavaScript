# JAVASCRIPT ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
Se ejecuta en el navegador del usuario, no en el servidor web
Aquí tienes los apuntes teóricos basados en los archivos proporcionados:

# Conceptos Teóricos y Ejemplos

## Variables y Tipos de Datos
- **Declaración de Variables**: En JavaScript, las variables pueden ser declaradas usando `var`, `let` o `const`.
  ```javascript
  var nombre = "Gregorio";
  nombre = "Gregorio";
  ```

- **Tipos de Datos**: JavaScript es un lenguaje dinámico, lo que significa que no es necesario declarar el tipo de dato al crear una variable. Ejemplo de diferentes tipos de datos:
  ```javascript
  var variable = 1; // Entero
  var variable2 = "2"; // Cadena
  var variable3 = 3.5; // Flotante
  ```

## Estructuras de Control
- **Condicionales**: Uso de `if`, `else if` y `else` para ejecutar diferentes bloques de código basado en condiciones.
  ```javascript
  if (confirm("Estas seguro?")) {
      alert("Sí");
  } else {
      alert("No");
  }
  ```

- **Bucles**: Uso de bucles `for` para repetir acciones múltiples veces.
  ```javascript
  for (var i = 0; i < 10; i++) {
      document.write("<br>" + i);
  }
  ```

## Interacciones con el Usuario
- **Alertas y Confirmaciones**: Uso de `alert`, `confirm` y `prompt` para interactuar con el usuario.
  ```javascript
  alert("Hola Mundo");
  var nombre = prompt("¿Cuál es tu nombre?");
  ```

## Manipulación del DOM
- **Escritura en el Documento**: Uso de `document.write` para escribir contenido directamente en la página web.
  ```javascript
  document.write("Hola <a href='https://gregoriofer.com'> Mundo </a>" + nombre);
  ```

- **Modificación de elementos del DOM**: Uso de `getElementsByTagName`, `getElementById` y `innerHTML` para acceder y modificar elementos del DOM.
  ```javascript
  window.onload = function(){
      let parrafos = document.getElementsByTagName("p");
      for(let i = 0; i < parrafos.length; i++){
          parrafos[i].onmouseover = cambiarColor;
      }
  }

  function cambiarColor(){
      this.style.backgroundColor = document.getElementById("id_color").value;
  }
  ```

- **Cambio de contenido dinámico**: Uso de `innerHTML` para modificar el contenido de los elementos del DOM.
  ```javascript
  function cargarParrafos(){
      let parrafos = document.getElementsByTagName("p");
      for (let i = 0; i < parrafos.length; i++) {
          parrafos[i].style.backgroundColor = "yellow";
          parrafos[i].innerHTML = i + " " + parrafos[i].innerHTML;
      }
  }
  ```

## Conversión de Tipos
- **Conversión de Cadenas a Números**: Uso de `parseInt` y `parseFloat` para convertir cadenas a números.
  ```javascript
  var numero = parseInt(prompt("Dame un número y te lo multiplico por 5"));
  document.write("El resultado es: " + numero * 5);
  ```

# Ejercicios Prácticos

## Ejercicio de Bucles
- **Tabla de Multiplicar**: Uso de bucles para generar una tabla de multiplicar.
  ```javascript
  for (var i = 1; i < 11; i++) {
      var num = 5;
      var calcular = num * i;
      document.write(num + " x " + i + " = " + calcular + "<br>");
  }
  ```

## Ejercicio de Encabezados
- **Generación de Encabezados**: Uso de bucles para generar encabezados de diferentes niveles.
  ```javascript
  for (var i = 1; i < 7; i++) {
      document.write("<h" + i + ">Hola mundo</h" + i + ">");
  }
  ```

## Ejercicio de Arreglos
- **Manejo de Arreglos**: Uso de arreglos para almacenar y mostrar diferentes tipos de datos.
  ```javascript
  var nombres = [33, true, 3.3, "Pedro", "Maria", "Ana", "Luis", "Carlos", "Rosa", "Laura"];
  document.write("<table border='1'>");
  for (var i = 0; i < nombres.length; i++) {
      document.write("<tr><td>" + nombres[i] + "</td></tr>");
  }
  document.write("</table>");
  ```

# Funciones

## Descripción
También se pueden crear funciones que realicen cualquier tipo de acción y llamarlas dentro del código principal.

## Ejemplo

```javascript
function suma(num1, num2) {
    return num1 + num2;
}
```

Llamado a la función `suma` con los parámetros `3` y `8`, guardando el resultado en la variable `sumandoNumeros`.

```javascript
let sumandoNumeros = suma(3, 8);
```

## Guardar datos de un formulario

```javascript
function recuperarDatos() {
    let n1 = parseInt(document.getElementById("numer1").value);
    let n2 = parseInt(document.getElementById("numer2").value);
    alert(suma(n1, n2));
}
```

### Formulario HTML

```html
<form>
    <input type="text" name="num1" id="numer1" value="0">
    <input type="text" name="num2" id="numer2" value="0">
    <input type="button" value="Sumar" onclick="recuperarDatos()">
</form>
```

Este formulario permite ingresar dos números en los campos de entrada y, al presionar el botón "Sumar", se ejecuta la función `recuperarDatos()`, que obtiene los valores de los campos, los convierte a enteros y muestra la suma en una alerta.

# Eventos usuales para modificar propiedades dentro de JavaScript

- onClick y onDblClick
- onLoad y onUnLoad
- onMouseOver y onMouseOut
- onMouseDown, onMouseMove y onMouseUp
- onChange
- onFocus y onBlur
- onKeyDown, onKeyUp y onKeyPress
- onSelect

