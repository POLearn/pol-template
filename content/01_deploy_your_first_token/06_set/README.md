# Interacción con un Contrato Inteligente

### Introducción

En esta última sección sobre el despliegue de tu primer contrato, aprenderemos cómo interactuar con tu contrato desplegado utilizando el método setter para actualizar la variable `name` 🔧

> Prerequisito: Asegúrate de tener MetaMask instalado y conectado a la red Open Campus Codex, y que tu contrato `SimpleContract` esté correctamente desplegado.

### Interactuar con el Contrato

Ahora que tu contrato `SimpleContract` está desplegado en la red Open Campus Codex, vamos a cambiar la variable `name` a **Vitalik** usando el método `set` y recuperar el hash de la transacción para verificar la transacción.

#### Llamar al Método `set`

Primero, localiza la función `set` en la interfaz de tu contrato. En el campo de entrada, escribe **Vitalik** y haz clic en "Transact." MetaMask te pedirá que confirmes la transacción; apruébala y espera a que la transacción sea procesada.

#### Verificar el Estado del Contrato

Una vez que la transacción sea confirmada, llama a la función `name` en tu contrato para verificar su valor actual. Si devuelve **Vitalik**, ¡felicitaciones! Has interactuado con éxito con tu contrato y actualizado su estado. 🎉

### ❗Enviar la Transacción a Proof of Learn

Para validar esta misión, envía el hash de la transacción a la plataforma Proof of Learn (POL). Esto confirma que has interactuado con éxito con el contrato inteligente.