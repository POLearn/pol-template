# Interacción con un Contrato Inteligente

Para esta última sección de desplegar tu primer contrato, aprendamos cómo interactuar con tu contrato desplegado utilizando el método setter para actualizar la variable `name` 🔧

> Prerrequisito: Asegúrate de tener MetaMask instalado y conectado a la red EDU Chain Testnet, y que tu contrato `SimpleContract` esté desplegado correctamente.

### Interactuar con el Contrato

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract.png)

Ahora que tu contrato `SimpleContract` está desplegado en la red EDU Chain Testnet, vamos a almacenar la variable `name` como `Vitalik` utilizando el método `set` y recuperar el hash de la transacción para verificarla.

### ❗Misión: Llamar al método `set`

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_set.png)

Puedes hacer clic en el método `set` en la interfaz de tu contrato. Dado que el contrato tiene un argumento, podrás ingresar el nombre. Ingresa el valor **Vitalik** y haz clic en *Enviar*. Esto te pedirá que confirmes la transacción y te permitirá aprobarla.

### Interactuar con el estado del contrato

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_name.png)

Una vez que la transacción sea confirmada, llama a la función `name` en tu contrato para comprobar su valor actual. Si devuelve `Vitalik`, ¡felicitaciones! Has interactuado con éxito con tu contrato y actualizado su estado. 🎉

Puedes enviar la transacción del método `set` a la plataforma Proof of Learn (POL) para esta misión. Esto confirma que has interactuado exitosamente con el contrato inteligente en EDU Chain.