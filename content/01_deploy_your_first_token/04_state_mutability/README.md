# Mutabilidad de Estado

### Introducción

La mutabilidad de estado en Solidity especifica cómo una función interactúa con el estado del contrato y la blockchain. Comprender la mutabilidad de estado es crucial para optimizar el uso de gas y garantizar que las funciones se comporten como se espera.

Existen tres tipos principales de mutabilidad de estado en Solidity: `pure`, `view` y `nonpayable`.

### Pure

Una función `pure` indica que no lee ni modifica el estado del contrato. Solo depende de sus parámetros de entrada y se utiliza típicamente para cálculos.

### View

Una función `view` permite leer el estado del contrato, pero prohíbe cualquier modificación. Puede utilizarse para acceder a los datos almacenados en el contrato sin cambiarlos.

### Nonpayable

Una función `nonpayable` puede modificar el estado del contrato y permite recibir Ether, pero no acepta ningún Ether durante la llamada. Es la mutabilidad de estado predeterminada si no se especifica ninguna.

Al utilizar la mutabilidad de estado correcta para tus funciones, puedes garantizar claridad en su comportamiento y optimizar los costos de gas para las interacciones de tu contrato.