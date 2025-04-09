# script_kiddie
Este repositorio está dedicado al aprendizaje y desarrollo de habilidades en el ámbito del hacking ético.
# Hacking & Cybersecurity Repository

Bienvenido a este repositorio dedicado al aprendizaje y práctica del hacking ético en diversas plataformas y entornos. Aquí encontrarás recursos, técnicas y guías sobre hacking en Linux, Active Directory y AWS.

## Contenido

- [Hacking en Linux](#hacking-en-linux)
  - [Comandos básicos de Linux](#comandos-básicos-de-linux)
  - [Post-explotación en Linux](#post-explotación-en-linux)
  - [Escalada de privilegios](#escalada-de-privilegios)

- [Hacking en entornos Windows: Enfoque en Active Directory](#hacking-en-entornos-windows-enfoque-en-active-directory)
  - [¿Qué es Active Directory?](#que-es-active-directory)
  - [Fases del hacking sobre Active Directory](#fases-del-hacking-sobre-active-directory) 


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
- se usa la flag `+x` para otorgar permiso de ejecución.
- ![image](https://github.com/user-attachments/assets/1c12e3ed-ea6b-4219-8b40-80a457f21b69)
- `chown` - Cambia el propietario de un archivo.
- ![image](https://github.com/user-attachments/assets/d2dbc42f-7a27-4251-bd03-6ea8e3809c25)
- `ps` / `top` - Muestra los procesos activos.
- ![image](https://github.com/user-attachments/assets/5869aa0d-fba1-4cd3-ba46-c619f7a41de3)
- `netstat` - Muestra conexiones de red.
- `ifconfig` / `ip a` - Muestra la configuración de red.
- ![image](https://github.com/user-attachments/assets/16ecd1d1-2c47-43b6-adef-c6de14163a6a)
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

# Hacking en entornos Windows: Enfoque en Active Directory
En esta fase se abordará el hacking ético en sistemas Windows, enfocándose específicamente en el **Active Directory (AD)**, un servicio crítico que se encuentra en la mayoría de entornos corporativos.

### ¿Qué es Active Directory?

**Active Directory (AD)** es un servicio de directorio desarrollado por Microsoft que se utiliza para gestionar y organizar usuarios, equipos y recursos dentro de una red.

Funciona como una **base de datos centralizada** que almacena información sobre todos los objetos en la red (usuarios, computadoras, grupos, permisos, etc.) y permite aplicar políticas de seguridad de forma eficiente.

# Fases del hacking sobre Active Directory

Cuando se realiza un análisis o ataque ético sobre un entorno con Active Directory, se siguen varias fases similares a las del hacking tradicional, pero con un enfoque específico en servicios y estructuras propias de Windows y el AD.

## 1. Reconocimiento

Se recopila información básica del entorno de Active Directory sin interactuar directamente con los sistemas.

### Técnicas comunes:
- Revisión de documentación interna (si se tiene acceso)
- OSINT sobre el dominio
- Identificación de nombres de dominio internos (por correos, metadatos, etc.)

## 2. Enumeración
Aquí se empieza a interactuar con la red para obtener más detalles del dominio y sus objetos.

### Herramientas comunes:
- `powerview`
- `rpcclient`
- `enum4linux`
- `CrackMapExec`
- `BloodHound` + `SharpHound`
- `ldapsearch`

### Información que se busca:
- Nombre del dominio
- Controladores de dominio
- Listado de usuarios
- Listado de equipos
- Delegaciones y relaciones de confianza
- Miembros de grupos privilegiados


## 3. Explotación de malas configuraciones
Se identifican y aprovechan errores comunes de configuración que permiten el acceso o la escalada de privilegios.

### Ejemplos:
- Usuarios con contraseñas débiles o predecibles
- Comparticiones SMB con permisos excesivos
- Delegaciones inseguras
- SPNs configurados incorrectamente
- Usuarios con permisos excesivos sobre objetos sensibles


## 4. Escalada de privilegios

A partir de una cuenta de usuario o acceso limitado, se intenta obtener privilegios más altos dentro del dominio.

### Ataques frecuentes:
- **Kerberoasting**
- **AS-REP Roasting**
- **Pass-the-Hash**
- **Pass-the-Ticket**
- **DCsync**
- **Abuso de ACLs (modificar objetos del AD)**


## 5. Movimiento lateral
Una vez con acceso elevado, se buscan otros equipos o cuentas dentro de la red para expandir el control.

### Técnicas:
- Uso de credenciales obtenidas para acceder a otros sistemas
- RDP, WinRM o SMB con usuarios privilegiados
- Uso de herramientas como `PsExec`, `CrackMapExec`, `Impacket`


## 6. Dominio comprometido (Domain Dominance)

Cuando se obtiene el control completo del dominio, ya sea como `Domain Admin` o con técnicas avanzadas como:

- **Golden Ticket**
- **Silver Ticket**


## 7. Persistencia y exfiltración
Se crean métodos para mantener el acceso y extraer información crítica sin ser detectado.

### Persistencia:
- Creación de cuentas ocultas
- Modificación de GPOs
- Backdoors en servicios

### Exfiltración:
- Robo de archivos sensibles
- Dump de bases de datos del AD
- Exfiltración usando canales encubiertos


Esta estructura es clave para entender cómo se analiza, ataca y compromete un entorno de Active Directory. En la siguiente sección se verán algunos de estos ataques aplicados en un entorno de laboratorio.

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

