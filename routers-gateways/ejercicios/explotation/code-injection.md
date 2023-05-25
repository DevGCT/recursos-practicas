# Inyección de código

En este documento se propone un ejemplo sencillo que permite ver el procedimiento para evaluar si un sistema es vulnerable a la inyección de código.

## Configuración del entorno de laboratorio

- Configura un entorno de laboratorio con un router Cisco simulado o virtualizado, como GNS3 o Cisco Packet Tracer.
- Asegúrate de tener acceso y permisos adecuados al router simulado para realizar cambios en su configuración.

## Acceso al router mediante Telnet

- Conéctate al router utilizando una aplicación de cliente Telnet, como PuTTY o el cliente Telnet incorporado en el sistema operativo.
- Ingresa la dirección IP del router y el número de puerto Telnet (generalmente el puerto 23) para establecer la conexión Telnet con el router.

## Identificación del campo vulnerable

Una vez conectado al router, identifica un campo de entrada que pueda ser propenso a la inyección de comandos, como un campo de configuración o un campo de ejecución de comandos. En este ejemplo, el campo de evaluación será el _command prompt_

## Prueba inicial de inyección de comandos

Intenta ingresar un comando válido seguido de un carácter especial, como una comilla simple (') o un punto y coma, para verificar si el campo es susceptible a la inyección de comandos.

Por ejemplo, ingresa alguno de los siguientes comandos en el campo vulnerable: 

`show interface FastEthernet0/0';` 

`show running-config';`

## Observa la respuesta del sistema

Observa la respuesta del sistema después de ingresar el comando con el carácter especial. Si el sistema devuelve una salida inesperada o muestra información confidencial, esto podría indicar una posible vulnerabilidad de inyección de comandos.
