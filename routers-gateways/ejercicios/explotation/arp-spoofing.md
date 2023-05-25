# ARP spoofing

## Configuración del entorno de laboratorio

Configura un entorno de laboratorio con dos equipos conectados a un switch o a una red simulada.  Asegúrate de tener acceso y permisos adecuados a los equipos y al switch o enrutador.

## Identificación de las direcciones IP y MAC

Identifica las direcciones IP y MAC del equipo víctima (por ejemplo, 192.168.0.100 y 00:11:22:33:44:55) y del equipo de destino (por ejemplo, 192.168.0.1 y AA:BB:CC:DD:EE:FF).
Puedes obtener esta información utilizando comandos como ipconfig en Windows o ifconfig en Linux.

Adicionalmente, se podría usar una herramienta como `ettercap` para el reconocimiento de posibles victimas

## Configuración del ataque

Abre una terminal en tu sistema y ejecuta el siguiente comando para iniciar el ataque de envenenamiento de ARP en el equipo víctima:

```
arpspoof -i <nombre de la interfaz> -t 192.168.0.100 192.168.0.1
```

Abre otra terminal y ejecuta el siguiente comando para envenenar la tabla ARP del equipo de destino:

```
arpspoof -i <nombre de la interfaz> -t 192.168.0.1 192.168.0.100
```

Esto hará que los equipos víctima y de destino crean que las direcciones MAC de los otros equipos están asociadas a sus respectivas direcciones IP.

## Monitoreo y observación

- Observa el tráfico de red y los efectos del ataque de envenenamiento de ARP.
- Puedes utilizar herramientas como Wireshark para capturar y analizar el tráfico de red y verificar cómo el envenenamiento de ARP afecta la comunicación entre los equipos.


