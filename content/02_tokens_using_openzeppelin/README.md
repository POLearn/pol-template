# Subiendo de Nivel: Desplegando un Token ERC20

¡Ahora que has desplegado e interactuado con tu primer contrato inteligente, es hora de llevar las cosas al siguiente nivel! En esta parte, te guiaremos para desplegar tu propio token ERC20, utilizando la implementación probada de OpenZeppelin. ¡Vamos a crear tu propio token en la red Open Campus Codex!

### ¿Qué es OpenZeppelin?

OpenZeppelin es una biblioteca para el desarrollo de contratos inteligentes seguros. Proporciona implementaciones de estándares populares de tokens, incluidos ERC20, que puedes usar para crear tus propios tokens sin tener que reinventar la rueda. Usar las implementaciones de OpenZeppelin garantiza que tu token siga las mejores prácticas y estándares en el ecosistema de Ethereum.

### Crear un `SampleERCToken`

Comencemos creando un contrato básico para el token ERC20, llamado `SampleERCToken`:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SampleERCToken {
}
```

### Importar ERC20 de OpenZeppelin

En tu archivo `TokenPoken.sol`, comienza importando la implementación de ERC20 de OpenZeppelin con la siguiente declaración:

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

Esto te permite heredar el contrato ERC20 y construir tu token sobre él. OpenZeppelin proporciona una base segura y probada para los tokens ERC20.

### Escribir el Contrato del Token

Ahora, define tu token ERC20 escribiendo el código del contrato. Usa el nombre "TokenPoken" y el símbolo "TP" como argumentos para el constructor ERC20. Asegúrate de que el constructor esté vacío, solo llamando al constructor `ERC20`:

Aquí tienes un ejemplo de código para comenzar:

```solidity
contract SampleERCToken is ERC20 { 
    constructor() ERC20("TokenPoken", "TP") {
        _mint(msg.sender, 1000000 * 10 ** decimals());
    }
}
```

Este código define la estructura básica de tu token, utilizando el contrato ERC20 de OpenZeppelin para garantizar seguridad y facilidad.

- **ERC20("TokenPoken", "TP")**: Esto establece el nombre y el símbolo de tu token.
- **_mint(msg.sender, 1000000 * 10 ** decimals())**: Minta 1 millón de tokens al creador del contrato (tu dirección).

### Compilar el Contrato

Para compilar, abre tu IDE de Solidity y selecciona la versión del compilador **0.8.23**. Haz clic en "Compilar" para asegurarte de que no haya errores. Un **check verde** confirmará una compilación exitosa.

### Desplegar el Contrato

Si estás usando el IDE de Solide, en la **pestaña Build & Deploy**, selecciona el contrato `SampleERCToken` y haz clic en **Deploy**.

### Probar Tu Token

Una vez que tu contrato `TokenPoken` esté desplegado, puedes interactuar con las funciones heredadas de ERC20. Aquí tienes algunas acciones para probar:

- 🧮 **Comprobar el suministro total:** Llama a `totalSupply` para ver el suministro total de tokens TokenPoken.
- 👛 **Verifica tu balance:** Usa `balanceOf` con tu dirección para ver tu saldo de tokens.
- 🔄 **Transferir Tokens:** Prueba la función `transfer` para enviar tokens a otra billetera.

### ❗Enviar el Despliegue a Proof of Learn

Si ya desplegaste un `SimpleContract` anteriormente, ahora puedes hacer lo mismo con el `SampleERCToken`. ¡Felicidades! Has creado y desplegado con éxito tu propio token ERC20 llamado TokenPoken con el símbolo TP utilizando el contrato ERC20 de OpenZeppelin. Este ejercicio demuestra el poder y la facilidad de usar OpenZeppelin para el desarrollo seguro y estandarizado de contratos inteligentes.

No olvides reclamar tu **POAP GRATUITO** en Proof of Learn, mostrando que has desplegado e interactuado con un contrato inteligente en Open Campus Codex. 🎉🎉🎉