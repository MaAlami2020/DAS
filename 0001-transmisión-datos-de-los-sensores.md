# Contexto y planteamiento del problema
Se quiere estudiar la transmisión de datos de varios sensores IoT
# Opciones consideradas

Estilo arquitectónico por eventos

Estilo arquitectónico modelo vista controlador (MVC)
# Resultado de la decisión
Se ha elegido el estilo arquitectónico por eventos porque el software se compone de 3 familias de sensores IoT, y una de las familias está compuesta por 3 sensores: uno que produce un evento transmitiendo datos sobre el estado de dispositivos físicos de la factoría; otro que recepciona los datos y los envía a un tercer sensor; y éste último, recepciona los datos del segundo sensor y los envía a un centro de notificaciones (Cockpit) para su análisis y almacenamiento en una base de datos SQL.
### Consequences

* Good, because tests are more readable
* Goop, because more easy to write tests
* Good, because more readable assertions
* Bad, because more complicated testing leads to more complicated assertions

## Pros and Cons of the Options

### Estilo arquitectónico por eventos

* Good, because Junit5 is "common Java knowledge"
* Bad, because complex assertions tend to get hard to read
* Bad, because no fluent API

### Estilo arquitectónico modelo vista controlador (MVC)

* Good, because Junit5 is "common Java knowledge"
* Bad, because complex assertions tend to get hard to read
* Bad, because no fluent API

