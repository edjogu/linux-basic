
Cheat Sheet: Permisos y chmod en Linux

Tabla de valores de permisos
| Permiso   | Letra | Valor |
|-----------|--------|--------|
| Lectura   | r      | 4      |
| Escritura | w      | 2      |
| Ejecución | x      | 1      |

Grupos de usuarios
| Grupo   | Letra | ¿Quién es?                  |
|---------|--------|-----------------------------|
| Usuario | u      | Propietario del archivo     |
| Grupo   | g      | Usuarios del mismo grupo    |
| Otros   | o      | Todos los demás usuarios    |

Ejemplos comunes de chmod
| Comando       | Permisos     | Significado                                          |
|---------------|--------------|------------------------------------------------------|
| chmod 755     | rwxr-xr-x    | Usuario todo, los demás leer y ejecutar              |
| chmod 700     | rwx------    | Solo el usuario puede todo                           |
| chmod 644     | rw-r--r--    | Usuario puede leer/escribir, otros solo leer         |
| chmod 600     | rw-------    | Solo el usuario puede leer/escribir                  |
| chmod 777     | rwxrwxrwx    | Todos pueden hacer todo (¡cuidado!)                  |

Modificadores simbólicos
| Comando          | Acción                                  |
|------------------|-----------------------------------------|
| chmod +x file    | Agrega ejecución a todos                |
| chmod u+x file   | Agrega ejecución solo al usuario        |
| chmod go-w file  | Quita escritura a grupo y otros         |
| chmod a+r file   | Agrega lectura a todos (a = all)        |

Ver permisos actuales
ls -l archivo

Salida:
-rwxr-xr-- 1 edjogu edjogu 1234 abr 10 update-tools.sh

Tip rápido:
| Número | Letras | Significado             |
|--------|--------|--------------------------|
| 7      | rwx    | Leer, escribir, ejecutar |
| 6      | rw-    | Leer, escribir           |
| 5      | r-x    | Leer, ejecutar           |
| 4      | r--    | Solo leer                |
| 0      | ---    | Sin permisos             |

<!-- Actualizado el 10 de abril de 2025 -->
