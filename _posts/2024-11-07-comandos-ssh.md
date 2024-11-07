---
layout: post
title:  "Comandos SSH"
categories: jekyll update
---

# Ejemplos de Scripts Básicos de SSH
## SSH (Secure Shell) es una herramienta esencial para la administración de servidores remotos y la automatización de tareas. A continuación se presentan algunos ejemplos básicos de scripts en Bash para utilizar SSH.

- Conectarse a un Servidor SSH
Para conectarse a un servidor remoto usando SSH:

```
ssh usuario@ip_o_dominio
```

- Conectarse con una Clave Privada Específica

```
ssh -i /ruta/a/clave_privada.pem usuario@ip_o_dominio
```

## Ejecutar un Comando en un Servidor Remoto
Este comando permite ejecutar instrucciones en el servidor remoto sin iniciar una sesión interactiva.

```
ssh usuario@ip_o_dominio "comando_a_ejecutar"
```

## Copiar Archivos de Forma Segura con scp

**Scp** permite copiar archivos entre la máquina local y el servidor remoto.

- Copiar un Archivo al Servidor

```
scp archivo.txt usuario@ip_o_dominio:/ruta/destino/
```

- Copiar un Archivo desde el Servidor

```
scp usuario@ip_o_dominio:/ruta/archivo.txt /ruta/destino/local
```