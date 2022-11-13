# Contexto y planteamiento del problema
Se quiere estudiar la transmisión de datos de varios sensores IoT
# Opciones consideradas
estilo arquitectónico por eventos
# Alternativas
estilo MVC
# Resultado de la decisión
Se ha tomado esta decisión porque el software se compone de 3 familias de sensores IoT, y una de las familias está compuesta por 3 sensores: uno que produce un evento transmitiendo datos sobre el estado de dispositivos físicos de la factoría; otro que recepciona los datos y los envía a un tercer sensor; y éste último, recepciona los datos del segundo sensor y los envía a un centro de notificaciones (Cockpit) para su análisis y almacenamiento en una base de datos SQL.
# Requisitos
RF.3 : recibir datos de los sensores
# Pros y Contras
(Pro) No hay un momento determinado en el cual un sensor tiene que recoger datos de un dispositivo físico o enviar datos a otro sensor o centro de control
(Pro) Un mismo sensor puede recoger datos de distintos dispositivos a la vez ya que se trata de un estilo arquitectónico asíncrono
