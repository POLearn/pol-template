# Desplegar un Contrato Inteligente

Después de cubrir los fundamentos de Solidity, incluyendo la estructura de contratos, variables de estado, definiciones de funciones y mutabilidad de estado, ¡es hora de desplegar el contrato `SimpleContract`! 🚀

### Agregar la Red EDU Chain a MetaMask

Para desplegar tu contrato en la red de prueba EDU Chain (EDU Chain Testnet), necesitarás agregar la red personalizada a MetaMask.

1. Abre MetaMask y haz clic en el desplegable de redes en la parte superior.
2. Selecciona "Agregar Red" y completa los siguientes detalles:

| **Campo**            | **Detalles**                                  |
|----------------------|----------------------------------------------|
| **Nombre de la Red** | EDU Chain Testnet                            |
| **Nuevo URL RPC**    | `https://open-campus-codex-sepolia.drpc.org` |
| **ID de la Cadena**  | `656476`                                     |
| **Símbolo de Moneda**| `EDU`                                        |
| **URL del Explorador de Bloques** | `https://edu-chain-testnet.blockscout.com/`   |

Una vez hayas agregado estos detalles, estarás conectado a la red EDU Chain Testnet y listo para desplegar tu contrato. 🎉

### Configuración del Contrato

Vamos a cargar la plantilla para nuestro contrato. Carga este contrato en tu IDE preferido. Idealmente, puedes usar el IDE interactivo de PoL. Simplemente proporcionando la URL: `https://github.com/POLearn/pol-template/blob/master/contracts/SimpleContract.sol`.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_load.png)

```solidity
string public name;

function set(string memory _name) public {
    name = _name;
}
```

¿Qué está pasando aquí?

La función `set` será la función de setter que permitirá a los usuarios actualizar la variable de estado `name` de forma dinámica. Toma un solo parámetro, `_name`, de tipo `string`, proporcionado durante la llamada a la función, y lo asigna a la variable `name` almacenada en el contrato. Esto hace que el contrato sea más interactivo, ya que permite actualizaciones en tiempo real, como renombrar un token o personalizar datos del contrato según la entrada del usuario.

### Compilar el Contrato

Asegúrate de estar utilizando la versión correcta del compilador de Solidity. Para este ejercicio, usaremos **0.8.23**. Es crucial usar la versión correcta, ya que las características y la sintaxis pueden variar entre versiones.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_version.png)

### Desplegar el Contrato

Una vez que tu contrato esté compilado, despliega el `SimpleContract` en la red EDU Chain Testnet que hemos conectado. MetaMask te pedirá aprobar la transacción para el despliegue.

Una vez confirmada la transacción, ¡tu contrato estará desplegado exitosamente! Has configurado MetaMask correctamente para la red EDU Chain Testnet y has desplegado un contrato inteligente. 🎉 También puedes conectar a la **Red Principal de EDU Chain (EDU Chain Mainnet)** con las siguientes configuraciones:

| **Campo**            | **Detalles**                                  |
|----------------------|----------------------------------------------|
| **Nombre de la Red** | EDU Chain                                    |
| **Nuevo URL RPC**    | `https://rpc.edu-chain.raas.gelato.cloud` |
| **ID de la Cadena**  | `41923`                                     |
| **Símbolo de Moneda**| `EDU`                                        |
| **URL del Explorador de Bloques** | `https://edu-chain.blockscout.com/`   |

### ❗Misión: Enviar el Contrato a PoL

Para completar esta misión en POL, envía la transacción de tu contrato desplegado a la plataforma Proof of Learn (POL). Esto confirma que has desplegado el contrato exitosamente. ¡Puedes ganar un 🏆**POL POAP**!

Ahora que tu contrato está desplegado, ¡es hora de profundizar más! En la siguiente sección, exploraremos cómo interactuar con tu contrato desplegado, actualizar la variable `name` y modificar el estado del contrato usando sus funciones ⚡