# script_kiddie
Este repositorio está dedicado al aprendizaje y desarrollo de habilidades en el ámbito del hacking ético.
# Hacking & Cybersecurity Repository

Bienvenido a este repositorio dedicado al aprendizaje y práctica del hacking ético en diversas plataformas y entornos. Aquí encontrarás recursos, técnicas y guías sobre hacking en Linux, Active Directory y AWS.

## Contenido

- [Hacking en Linux](#hacking-en-linux)
  - [Comandos básicos de Linux](#comandos-básicos-de-linux)
  - [Post-explotación en Linux](#post-explotación-en-linux)
  - [Escalada de privilegios](#escalada-de-privilegios)

- [Hacking en entornos Windows: Enfoque en Active Directory](#hacking-en-active-directory)
  - [Enumeración en Active Directory](#enumeración-en-active-directory)
  - [Ataques de Kerberos](#ataques-de-kerberos)
  - [Escalada de privilegios en AD](#escalada-de-privilegios-en-ad)
  - [Persistence y Dominación](#persistence-y-dominación)

- [Hacking en AWS](#hacking-en-aws)
  - [Enumeración y reconocimiento](#enumeración-y-reconocimiento)
  - [Explotación de IAM](#explotación-de-iam)

---

## Hacking en Linux

### Comandos básicos de Linux
- `ls` - Lista los archivos y directorios.
- ![image](https://github.com/user-attachments/assets/cddb6fdf-d552-4027-a2d0-0e2fa564426f)
- `cd` - Cambia de directorio.
- ![image](https://github.com/user-attachments/assets/990fbd17-6077-483e-bb75-0067b9ef470d)
- `pwd` - Muestra la ruta del directorio actual.
- ![image](https://github.com/user-attachments/assets/142549ff-ffca-437c-be5c-86d73db687b3)
- `cp` - Copia archivos o carpetas.
- Se indica el nombre del archivo a copiar, luego se indica la ruta del directorio en cual se copiara.
- ![image](https://github.com/user-attachments/assets/986754c0-9cb5-4bd6-a34d-605e363aca7e)
- `mv` - Mueve o renombra archivos.
- Se indica el nombre del archivo a mover o renombrar, seguido la ruta del directorio destino o su nuevo nombre.
- ![mv](https://github.com/user-attachments/assets/c1c17f0a-98be-4395-a827-48028bb988b6)
- `rm` - Elimina archivos o carpetas.
- ![rm](https://github.com/user-attachments/assets/065b9afb-42b0-496d-b070-e814903a0e23)
- `chmod` - Cambia los permisos de los archivos.
- `chown` - Cambia el propietario de un archivo.
- `ps` / `top` - Muestra los procesos activos.
- `netstat` - Muestra conexiones de red.
- `ifconfig` / `ip a` - Muestra la configuración de red.
- `grep` - Busca texto en archivos.
- `find` / `locate` - Busca archivos en el sistema.
- `tar` / `gzip` / `zip` - Comprime y descomprime archivos.
- `echo` / `cat` - Muestra contenido en la terminal.

### Post-explotación en Linux
- Técnicas para mantener el acceso en sistemas Linux comprometidos.

### Escalada de privilegios
- Explotación de binarios con `SUID` y `sudo` mal configurados.
- ```sudo -l ``` `sudo su`
- Vulnerabilidades Kernel y explotación de `CVE` relevantes.

---

## Hacking en entornos Windows: Enfoque en Active Directory
- En esta fase se abordará el hacking ético en sistemas Windows, enfocándose específicamente en el **Active Directory (AD)**, un servicio crítico que se encuentra en la mayoría de entornos corporativos.

### ¿Qué es Active Directory?

**Active Directory (AD)** es un servicio de directorio desarrollado por Microsoft que se utiliza para gestionar y organizar usuarios, equipos y recursos dentro de una red.

Funciona como una **base de datos centralizada** que almacena información sobre todos los objetos en la red (usuarios, computadoras, grupos, permisos, etc.) y permite aplicar políticas de seguridad de forma eficiente

## Componentes principales

- **Controlador de Dominio (Domain Controller):** Es el servidor principal que ejecuta el servicio de Active Directory. Se encarga de autenticar usuarios y aplicar políticas.
- **Dominio:** Es el entorno lógico en el que se agrupan todos los objetos gestionados por AD. Cada dominio tiene al menos un controlador.
- **Objetos:** Todo lo que administra el AD se considera un "objeto", como:
  - Usuarios
  - Computadoras
  - Grupos
  - Unidades Organizativas (OU)
- **GPO (Group Policy Objects):** Son políticas que permiten configurar el comportamiento del sistema operativo, restringir funciones, establecer contraseñas obligatorias, entre otras.
- **LDAP (Lightweight Directory Access Protocol):** Es el protocolo que utiliza AD para consultar y modificar la información en el directorio.
- **Kerberos:** Es el protocolo principal que utiliza AD para la autenticación de usuarios y servicios.

## ¿Qué se puede hacer con Active Directory?

- Crear y eliminar cuentas de usuarios y equipos.
- Administar permisos sobre usuarios, carpetas, impresoras, aplicaciones, etc. 
- Aplicar políticas de seguridad en toda la red.

## Ventajas para las empresas

- **Centralización:** Todo se gestiona desde un solo lugar.
- **Seguridad:** Permite establecer políticas de acceso y control granular.
- **Escalabilidad:** Funciona desde pequeñas redes hasta grandes corporaciones.
- **Automatización:** Muchas tareas administrativas se pueden automatizar.

---

Active Directory es una de las piezas más críticas de la infraestructura en muchas organizaciones, lo que lo convierte en un objetivo clave tanto para la administración como para los posibles atacantes.


### Ataques de Kerberos
- Pass-the-Ticket y Kerberoasting.
- AS-REP Roasting y `OverPass-the-Hash`.

### Escalada de privilegios en AD
- Uso de `Privilege Escalation Paths` en AD.
- Abuso de permisos en `Active Directory ACLs`.

### Persistence y Dominación
- Uso de `Golden Ticket` y `Silver Ticket`.
- Creación de usuarios persistentes en AD.

---

## Hacking en AWS

### Enumeración y reconocimiento
- Uso de `awscli`.

### Explotación de IAM
- Extracción y abuso de credenciales en `AWS IAM`.
- Uso de `Lambda`, `EC2` y `S3` para acceso persistente.

---

## Requisitos y Herramientas
- **Linux:** Kali Linux, ParrotOS.
- **Active Directory:** Windows Server 2016/2019, BloodHound, Mimikatz.
- **AWS:** AWS CLI.

##  Recursos y Referencias
- [HackTricks](https://book.hacktricks.xyz/)


---

⚠️ Este repositorio es solo para fines educativos y de aprendizaje. El uso indebido de estas técnicas es ilegal.

