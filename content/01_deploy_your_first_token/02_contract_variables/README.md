# Tipos Básicos de Solidity

### Introducción

¡Vamos a sumergirnos en los bloques fundamentales de los contratos inteligentes explorando las variables básicas del contrato que definen su estado y comportamiento!

En Solidity, las variables son de tipo estático, lo que significa que debes definir su tipo al declararlas, asegurando claridad y estructura en tus contratos inteligentes. Estas variables pueden tomar valores predeterminados según su tipo, y Solidity ofrece una variedad de tipos elementales, desde enteros y booleanos hasta direcciones y estructuras personalizadas, permitiéndote modelar datos complejos de manera efectiva.

**Ejemplos de Tipos de Solidity**

-   **uint**: Entero sin signo
-   **int**: Entero con signo
-   **bool**: Valor booleano
-   **address**: Dirección de Ethereum
-   **string**: Cadena de texto
-   **bytes**: Arreglo de bytes de tamaño fijo
-   **struct**: Estructura de datos personalizada
-   **enum**: Tipo definido por el usuario para valores enumerados

### uint

Un entero sin signo que puede representar números enteros no negativos, lo que permite valores más grandes sin el riesgo de números negativos.

  ```solidity
  uint256 count = 10; 
  ```

### int

Un entero con signo que puede representar tanto números enteros positivos como negativos, útil para cálculos que requieren un rango de valores.

  ```solidity
  int256 balance = -50; 
  ```

### bool

Un valor booleano que puede ser `true` o `false`, comúnmente utilizado para declaraciones condicionales y banderas.

  ```solidity
  bool isActive = true; 
  ```

### address

Un tipo de datos que representa una dirección de Ethereum, crucial para identificar cuentas y contratos inteligentes en la blockchain.

  ```solidity
  address owner = 0x1234567890abcdef1234567890abcdef12345678; 
  ```

### string

Una secuencia dinámica de caracteres utilizada para almacenar texto, permitiendo longitudes flexibles y variables de datos de texto.

```solidity
  string greeting = "¡Hola, blockchain!"; 
  ```

### bytes

Un arreglo de bytes de tamaño fijo utilizado para almacenar datos binarios sin procesar, proporcionando una manera eficiente de gestionar datos a nivel de bytes.

```solidity
  bytes32 data = 0xabcdefabcdefabcdefabcdefabcdefabcdefabcdef; 
  ```

> 👀 Solidity ofrece varios tipos básicos de variables, cada una con su valor predeterminado: **`uint`** (entero sin signo) se inicializa a `0`, **`int`** (entero con signo) también se inicializa a `0`, **`bool`** (booleano) se inicializa a `false`, **`address`** se inicializa a la dirección cero (`0x0000000000000000000000000000000000000000`), **`string`** se inicializa a una cadena vacía (`""`), y **`bytes`** se inicializa a un arreglo de bytes vacío. Por ejemplo:
> ```solidity
> uint256 count;        // Predeterminado: 0
> int256 balance;       // Predeterminado: 0
> bool isActive;        // Predeterminado: false
> address owner;        // Predeterminado: 0x000...
> string greeting;      // Predeterminado: ""
> bytes32 data;         // Predeterminado: ""
> ```

### Tarea 📝

Con el `SimpleContract` compilado, añade una variable pública de tipo string llamada `name` que cualquiera pueda acceder:

```solidity
string public name; // Esta variable almacenará el nombre
```