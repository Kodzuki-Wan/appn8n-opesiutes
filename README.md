# appn8n-opesiutes
Repositorio del código del proyecto para la automatización del envió del código de seguridad a través de WhatsApp al huésped.

# Análisis del Problema
Actualmente, la gestión de acceso a las habitaciones se realiza de forma manual mediante la aplicación Salto KS. Esto crea una dependencia del personal para la creación y el envío de los códigos de seguridad, lo que genera retrasos y posibles errores en el proceso.

# Propuesta de Solución
La solución propuesta es automatizar el proceso de la siguiente manera:

1. Creación de un formulario: Se diseñará un formulario alimentado por las bases de datos de reservas de Cloudbeds y Salto KS. Este formulario mostrará una lista de huéspedes y habitaciones disponibles, y tendrá los siguientes campos:
- Nombre del huésped
- Identificación
- Número de habitación (lista desplegable)
- Valor a pagar
- Estado de pago (Completo/Parcial)
- Botón para  enviar el código

Automatización del envío: Una vez completado el formulario, se establecerá una conexión con la API de Salto KS. A través de esta API, se solicitará el código de acceso de la habitación seleccionada y se enviará automáticamente al huésped por WhatsApp, facilitando su ingreso.

# Retos y Pendientes
- API de Salto KS: Aún no se ha confirmado el acceso a la API. Estamos a la espera de la comunicación del proveedor para su validación.
   - Plan B: En caso de no obtener acceso a la API, se evaluarán otras alternativas como la creación de una macro de automatización o el uso de web scraping.
-    Servicio de formulario: Se está evaluando la plataforma para el formulario. Se considera Google Sheets (en lugar de Docs, ya que es más funcional para bases de datos y automatización) como una de las opciones principales.

