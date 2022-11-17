# Contexto y planteamiento del problema

Se quiere estudiar la transmisión de datos de varios sensores IoT

# Opciones consideradas

estilo arquitectónico por eventos

# Alternativas

Estilo arquitectónico modelo vista controlador (MVC)

# Resultado de la decisión

Se ha tomado esta decisión porque el software se compone de 3 familias de sensores IoT, y una de las familias está compuesta por 3 sensores: uno que produce un evento transmitiendo datos sobre el estado de dispositivos físicos de la factoría; otro que recepciona los datos y los envía a un tercer sensor; y éste último, recepciona los datos del segundo sensor y los envía a un centro de notificaciones (Cockpit) para su análisis y almacenamiento en una base de datos SQL.

# Requisitos

RF.3 : recibir datos de los sensores

# Pros y Contras

(Pro) No hay un momento determinado en el cual un sensor tiene que recoger datos de un dispositivo físico o enviar datos a otro sensor o centro de control
(Pro) Un mismo sensor puede recoger datos de distintos dispositivos a la vez ya que se trata de un estilo arquitectónico asíncrono

### Estilo arquitectónico por eventos

#### Ventajas

- Simplicidad
- Evolución: se pueden reemplazar componentes suscriptores
- Modularidad: una sola modalidad para eventos diversos
- Puede mejorar la eficiencia, eliminando la necesidad de polling por ocurrencia de evento

#### Desventajas

- Posibilidad de desborde
- Potencial imprevisión de escalabilidad
- Pobre comprensibilidad: Puede ser difícil prever qué pasará en respuesta a una acción
- No hay garantía del lado del publicador, que el suscriptor responderá al evento
- No hay mucho soporte de recuperación en caso de falla parcial

### Estilo arquitectónico modelo vista controlador (MVC)

#### Ventajas

- La separación del Modelo y la Vista, lo cual logra separar los datos, de su representación visual.
- Facilita el manejo de errores.
- Permite que el sistema sea escalable si es requerido.
- Es posible agregar múltiples representaciones de los datos.

#### Desventajas

- La cantidad de archivos que se deben mantener incrementa considerablemente.
- La curva de aprendizaje es más alta que utilizando otros modelos.
- Su separación en capas, aumenta la complejidad del sistema.
