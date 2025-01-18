# Desplegar un Token ERC20

Con una comprensión básica de los contratos inteligentes y el uso de EDU Chain para interactuar con ellos, ¡es hora de llevar las cosas un paso más allá! En esta sección, te guiaremos para desplegar tu propio **token ERC20**, utilizando la implementación probada de OpenZeppelin para ERC20 🪙.

### ¿Qué es OpenZeppelin?

Antes de sumergirnos en el contrato, entendamos qué es OpenZeppelin. OpenZeppelin es una biblioteca para el desarrollo de contratos inteligentes seguros. Proporciona implementaciones de estándares populares de tokens, incluido ERC20, que puedes usar para crear tus propios tokens sin tener que reinventar la rueda. Usar las implementaciones de OpenZeppelin asegura que tu token cumpla con las mejores prácticas y estándares del ecosistema Ethereum.

Ahora que entendemos la estructura básica del contrato, vamos a crear un `SampleERCToken`. Carga el contrato de plantilla [aquí](https://github.com/POLearn/pol-template/blob/master/contracts/SampleERCToken.sol) en tu IDE deseado.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_load.png)

Podemos ver que es un contrato vacío. Sin embargo, es importante destacar que se importa el contrato `ERC20` de OpenZeppelin. Veamos ese fragmento de código:

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

Esto te permite heredar el contrato ERC20 y construir tu token sobre él. OpenZeppelin proporciona una base segura y probada para los tokens ERC20.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_setup.png)

Si miramos el constructor, vemos que toma un `name` y un `symbol`. El resto del código son implementaciones para acuñar y transferir el token ERC20, todo completado por ti.

Ahora, hereda esto en tu contrato principal. Regresa a `SampleERCToken` y asegúrate de que tu contrato sea `ERC20`, de manera que quede como:

```solidity
contract SampleERCToken is ERC20
```

En el constructor, también nos aseguraremos de llamar al constructor de ERC20:

```solidity
constructor() ERC20("TokenName", "TOKEN") {
}
```

Definiremos el token ERC20 escribiendo el código del contrato. Usa el nombre "TokenPoken" y el símbolo "TP" como argumentos para el constructor de ERC20. Asegúrate de que el constructor esté vacío, llamando solo al constructor `ERC20`:

Para más detalles sobre el contrato ERC20, consulta la [documentación de OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/erc20) para entender sus características y funcionalidades.

### Compilar el Contrato

Como en el contrato anterior, asegúrate de estar usando la versión correcta del compilador de Solidity. Para este ejercicio, utilizaremos **0.8.23**. Usar la versión correcta es crucial, ya que las características y la sintaxis pueden variar entre versiones.

### Desplegar el Contrato

Una vez que tu contrato esté compilado, despliega el `SampleERCToken` en la red de pruebas de EDU Chain a la que nos conectamos. MetaMask te pedirá aprobar la transacción para el despliegue.

### Probar Tu Token

Una vez que tu contrato `TokenPoken` esté desplegado, puedes interactuar con sus funciones heredadas de ERC20. Aquí hay algunas acciones para probar:

- 🧮 **Consultar el Suministro Total:** Llama a `totalSupply` para ver el suministro total de tokens TokenPoken.
- 👛 **Consultar tu Saldo:** Usa `balanceOf` con tu dirección para ver tu saldo de tokens.
- 🔄 **Transferir Tokens:** Prueba la función `name` para enviar tokens a otra billetera.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_name.png)

### ❗Misión: Despliegue del Token

Si ya desplegaste un `SimpleContract` anteriormente, puedes hacer lo mismo con `SimpleERCToken`. ¡Felicidades! Has creado y desplegado con éxito tu propio token ERC20 llamado TokenPoken con el símbolo TP utilizando el contrato ERC20 de OpenZeppelin. Este ejercicio demuestra el poder y la facilidad de usar OpenZeppelin para el desarrollo seguro y estandarizado de contratos inteligentes.

Asegúrate de reclamar tu **POL POAP** de Proof of Learn, ¡demostrando que has desplegado e interactuado con un contrato inteligente en EDU Chain! 🎉🎉🎉