# Contexto y planteamiento del problema

Un componente de visualización que muestre las analísticas en tiempo real del proceso productivo y las órdenes de trabajo.

# Opciones consideradas

Estilo arquitectónico modelo vista controlador (MVC)

# Alternativas

# Resultado de la decisión

Se ha tomado esta decisión porque el software

# Requisitos

RF.1 : Visualización de estadisticas

# Pros y Contras

(Pro) Ayuda dividir forntend con backend

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
