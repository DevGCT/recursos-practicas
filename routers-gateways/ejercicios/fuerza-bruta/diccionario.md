# Ataque de diccionario con Hydra

## Instala Hydra
Asegúrate de tener Hydra instalado en tu sistema. Puedes descargarlo desde la página oficial de Hydra o utilizar el administrador de paquetes de tu sistema operativo.

```bash
sudo apt install hydra
```

## Obten la información de destino
Antes de ejecutar el ataque, necesitas recopilar información sobre el objetivo, como el nombre de usuario o la URL del formulario de inicio de sesión.

# Crear un diccionario
Prepara un archivo de texto que contenga una lista de posibles contraseñas que se probarán en el ataque. Puedes incluir contraseñas comunes, palabras clave relevantes o personalizarlo según tus necesidades.

# Ejecuta el ataque de diccionario 
Abre una terminal y ejecuta el siguiente comando:

```
hydra -l <nombre_de_usuario> -P <ruta_al_diccionario> <dirección_del_objetivo> <protocolo>
```

- Reemplaza <nombre_de_usuario> con el nombre de usuario o lista de nombres de usuario a probar.
- Reemplaza <ruta_al_diccionario> con la ruta al archivo de diccionario que creaste.
- Reemplaza <dirección_del_objetivo> con la dirección IP o URL del objetivo.
- Reemplaza <protocolo> con el protocolo de autenticación utilizado, como HTTP, FTP, SSH, etc.

Por ejemplo, si deseas realizar un ataque de diccionario HTTP a un formulario de inicio de sesión con el nombre de usuario "admin" y utilizando un archivo de diccionario llamado "diccionario.txt", el comando podría ser:

```
hydra -l admin -P diccionario.txt http://example.com/login
```
También es valido hacerlo de la siguiente manera

```
hydra -L users.txt -P diccionario.txt 192.168.1.111 ssh
```

# Monitorear el progreso y los resultados
Hydra mostrará el progreso y los intentos de autenticación que está realizando. Puedes monitorear la salida en tiempo real y ver si se encuentra una coincidencia de contraseña exitosa.

Recuerda que es importante realizar este tipo de actividad solo con el consentimiento del propietario del sistema o con fines educativos legítimos.
