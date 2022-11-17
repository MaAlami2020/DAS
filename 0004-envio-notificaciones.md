# Contexto y planteamiento del problema

Envío de notificaciones por mensajería interna a los operarios

# Opciones consideradas

Patrón Publisher - Subscriber

# Resultado de la decisión

El motivo de esta decisión es que permite que la aplicacion anuncie eventos de forma asíncrona, solo a los receptores interesados.

# Requisitos

RF.4 : Envio de notificaciones

# Pros y contras

(Pro) Puedes introducir nuevos tipos de subscriptores sin tener que cambiar el notificador
