# Simulación de un ataque DoS

## Configuración del entorno de laboratorio

Configura un entorno de laboratorio con un router Cisco simulado o virtualizado, como GNS3 o Cisco Packet Tracer.
Asegúrate de tener acceso y permisos adecuados al router simulado para realizar cambios en su configuración.

## Instalación de Hping3

Descarga e instala la herramienta Hping3 en tu sistema. Puedes encontrar versiones disponibles para diferentes sistemas operativos en el sitio web oficial.

```
sudo apt install hping3
```

## Identificación del destino y configuración del ataque

Identifica la dirección IP del router que deseas atacar. A continuación, configura Hping3 con los parámetros adecuados para realizar el ataque. Por ejemplo, puedes utilizar el siguiente comando:

```
hping3 --flood -p 80 <dirección IP del router>
```

## Ejecución del ataque

Ejecuta el comando configurado para iniciar el ataque de denegación de servicio. Hping3 enviará una gran cantidad de paquetes TCP al puerto 80 del router, abrumando su capacidad de procesamiento y causando una interrupción en los servicios.

Observa los efectos del ataque en el router objetivo. Puedes monitorear la respuesta del router y verificar si los servicios se ven afectados o si se produce una degradación significativa en su rendimiento.
