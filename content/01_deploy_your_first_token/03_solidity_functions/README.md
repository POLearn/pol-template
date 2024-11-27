# Funciones

### Introducción

Ahora que tenemos un contrato configurado con algunas variables de estado, vamos a sumergirnos en cómo podemos usar funciones para interactuar con ellas.

### Definición de Función

Antes de poder usar una función en nuestro `SimpleContract`, necesitamos definirla. En Solidity, las funciones se definen utilizando la palabra clave `function`, seguida de un nombre único para la función, una lista opcional de parámetros y un bloque de instrucciones encerrado entre llaves. La **sintaxis básica** es:

```solidity
function functionName(int arg1, string memory arg2, ...) visibilidad mutabilidadEstado retorna() {
   // La lógica va aquí :)
}
```

### Nombre de la Función

Este declara la función con un nombre único (`functionName`), que es cómo la llamarás.

### Parámetros

Esta parte especifica los parámetros de la función, donde `arg1` es un entero y `arg2` es una cadena almacenada en memoria; se pueden incluir parámetros adicionales según sea necesario.

### Visibilidad

Esto define el nivel de acceso de la función, como `public`, `private` o `internal`, determinando quién puede llamar a la función.

### Mutabilidad de Estado

> ⚠️**Nota:** ¡Abordaremos el concepto de alcance (scope) en el siguiente recurso!

Esto indica si la función puede modificar el estado del contrato (por ejemplo, `pure`, `view` o `nonpayable`), lo que afecta cómo interactúa con la blockchain.

### Tipos de Retorno

Esto especifica el tipo de retorno de la función, indicando qué valor devolverá cuando se llame; los paréntesis pueden contener el tipo si la función devuelve un valor.

Por ejemplo, `returns(uint)` significa que la función devolverá un entero sin signo.

```solidity
function getValue() public view returns(uint) {
	return 1;
}
```

### Tarea 📝

Añade la siguiente función a tu `SimpleContract` para permitir que los usuarios configuren la variable de estado `name`:

```solidity
function set(string memory _name) public;
```

Esta función toma un parámetro de tipo cadena `_name` y actualiza la variable `name` en el contrato.