# Configuración de un Contrato Inteligente

### Introducción

En esta sección, repasaremos la estructura básica de un contrato inteligente, que permite automatizar acuerdos y transacciones en la blockchain, ¡abriendo el camino para aplicaciones descentralizadas innovadoras!

### Identificador de Licencia

```solidity
// SPDX-License-Identifier: MIT
```

Típicamente, la primera línea es un **Identificador de Licencia**, que es opcional, pero una buena práctica. Al usar la licencia MIT, animamos a otros a utilizar y modificar libremente nuestro contrato inteligente, al mismo tiempo que aclaramos los permisos legales involucrados, fomentando la colaboración en la comunidad blockchain.

### Directiva Pragma

La **directiva pragma** especifica la versión del compilador de Solidity a utilizar:

```solidity
pragma solidity ^0.8.20;
```

En este caso, `^0.8.20` asegura que el contrato se compile con la versión 0.8.20 o versiones más recientes que no introduzcan cambios incompatibles. Esto ayuda a mantener la compatibilidad y garantiza que el contrato funcione como se espera.

### Declaración del Contrato

Este fragmento define un contrato básico llamado `SimpleContract`. La palabra clave `contract` se usa para declarar un nuevo contrato en Solidity, que sirve como plantilla para crear instancias de ese contrato en la blockchain.

Dentro de las llaves `{}`, es donde se implementará toda la lógica y funcionalidad del contrato. Esto puede incluir variables de estado, funciones y cualquier otro elemento necesario para definir el comportamiento del contrato.

```solidity
contract SimpleContract { 
	// Toda la lógica va aquí :) 
}
```

### Compilando el Contrato

Para compilar tu contrato inteligente, es esencial seleccionar la versión correcta del compilador de Solidity que coincida con la directiva pragma, como `pragma solidity ^0.8.20;`. Elegir una versión compatible, como **0.8.20** o más reciente, asegura una compilación exitosa que genera:

-   🛠️ **Bytecode** para el despliegue en la blockchain
-   📡 **Interfaz Binaria de Aplicación (ABI)** para interactuar con las funciones y eventos del contrato

En conclusión, usar la versión correcta del compilador es crucial para el despliegue y funcionamiento de tu contrato inteligente.