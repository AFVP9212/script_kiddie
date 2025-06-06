# script_kiddie Red Team
Este repositorio está dedicado al aprendizaje y desarrollo de habilidades en el ámbito del hacking ético.
Aquí encontrarás recursos, técnicas y guías sobre hacking en Linux, Active Directory y AWS.

## Contenido

- [Hacking en Linux](#hacking-en-linux)
  - [Distribuciones de linux orientadas a la ciberseguridad y hacking](#distribuciones-de-linux-orientadas-a-la-ciberseguridad-y-hacking)
  - [Comandos básicos en Linux](#comandos-básicos-de-linux)
  - [Servicios básicos en Linux](#servicios-básicos-en-linux)
  - [Herramientas de enumeración en Linux](#herramientas-de-enumeración-en-linux)
  - [Herramientas de explotación en Linux](#herramientas-de-explotación-en-linux)
  - [Escalamiento de privilegios](#escalamiento-de-privilegios)
  - [Post-explotación en Linux](#post-explotación-en-linux)
  

- [Hacking en entornos Windows: Enfoque en Active Directory](#hacking-en-entornos-windows-enfoque-en-active-directory)
  - [Fases del hacking sobre Active Directory](#fases-del-hacking-sobre-active-directory)
  - [Documentación de vulnerabilidades en AD](#documentación-de-vulnerabilidades-en-ad)


- [Hacking en AWS](#hacking-en-aws)
  - [Enumeración y reconocimiento](#enumeración-y-reconocimiento)
  - [Comandos utiles en awscli](#comandos-utiles-en-awscli)
  - [Explotación de IAM](#explotación-de-iam)
  - [Documentación sobre hacking en aws](#documentación-sobre-hacking-en-aws)

- [Vulnerabilidades Web](#vulnerabilidades-web)
  - [Herramientas de explotación Web](#herramientas-de-explotación-web)

- [Descarga nuestra maquina virtual](#descarga-nuestra-maquina-virtual)

- [Requisitos y Herramientas](#requisitos-y-herramientas)

- [Recursos y Referencias](#recursos-y-referencias)

- [Sitios web para aprender a resolver CTFs](#sitios-web-para-aprender-a-resolver-ctfs)

- [Sitios web de documentación de vulnerabilidades](#sitios-web-de-documentación-de-vulnerabilidades)
---

## Hacking en Linux

### Distribuciones de linux orientadas a la ciberseguridad y hacking

| Distribución         | Enlace oficial                              | Enfoque principal                             |
|----------------------|---------------------------------------------|-----------------------------------------------|
| Kali Linux           | [kali.org](https://www.kali.org)            | Pentesting y auditoría de seguridad           |
| Parrot Security OS   | [parrotsec.org](https://www.parrotsec.org)  | Privacidad, desarrollo, análisis forense      |
| BlackArch Linux      | [blackarch.org](https://www.blackarch.org)  | Pentesting avanzado basado en Arch            |


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

### Escalamiento de privilegios
- Explotación de binarios con `SUID` y `sudo` mal configurados.
- Web recomendada para la explotacion de binarios: [GTFOBins](https://gtfobins.github.io/)
- ```sudo -l ``` `sudo su` para la comprobación de permisos que tiene el usuario.
- Vulnerabilidades Kernel y explotación de `CVE` relevantes.
- Web recomendada para buscar vulnerabilidades de kernel y explotaciones: [Exploit Database](https://www.exploit-db.com/)

### Servicios básicos en Linux
- `ssh` - Protocolo para conexión remota segura.
- `apache2` / `nginx` - Servidores web comunes.
- `mysql` / `postgresql` - Sistemas de gestión de bases de datos.
- `cron` - Programación de tareas automáticas.
- `rsyslog` / `journald` - Servicios de logging.
- `ufw` / `firewalld` - Control de firewall.
- `vsftpd` - Servidor FTP seguro.

### Herramientas de enumeración en Linux
- `linpeas` - Script de enumeración para escalada de privilegios.
- Descarga [linpeas](https://github.com/peass-ng/PEASS-ng/releases/tag/20250401-a1b119bc)
- `pspy` - Monitorea procesos sin requerir privilegios root.
- `netstat` / `ss` - Inspección de puertos y conexiones.
- `lsof` - Verifica archivos abiertos.
- `enum4linux` - Recolección de información sobre servicios Samba.
- `nmap` - Escaneo de puertos y servicios.

### Herramientas de explotación en Linux
- `exploitdb` - Base de datos de exploits públicos.
- `searchsploit` - Busca exploits en la base de datos local.
- `Metasploit Framework` - Plataforma de desarrollo de exploits.
- `GTFObins` - Recolección de binarios que pueden ser explotados.
- `pwndbg` + `gdb` - Depuración avanzada para binarios vulnerables.
- `dirtycow`, `overlayfs`, `polkit` - Ejemplos de exploits locales.
- `revshells.com` - Sitio web para generar *reverse shells* automáticamente en diferentes lenguajes (bash, python, php, powershell, etc).

### Post-explotación en Linux
- Técnicas para mantener el acceso en sistemas Linux comprometidos.
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

### Documentación de vulnerabilidades en AD
- [Hacking Articles](https://www.hackingarticles.in/)
- [Harmj0y Blog](https://www.harmj0y.net/blog/)
- [SpecterOps Blog](https://posts.specterops.io/)
- [AdSecurity](https://adsecurity.org/)

---

## Hacking en AWS

### Enumeración y reconocimiento
- Uso de `awscli`.
- Aqui podremos descargar la [awscli](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
- Uso de la metadata con la dirección: http://169.254.169.254

### Comandos utiles en awscli
- Aqui se podran consultar [comandos utiles](https://github.com/0x04e1/AWS-Enum) en la `awscli`.

### Explotación de IAM
- Extracción y abuso de credenciales en `AWS IAM`.
- Uso de `Lambda`, `EC2` y `S3` para acceso persistente.

### Documentación sobre hacking en aws.
- [Ethical Hacking en AWS](https://books.spartan-cybersec.com/cpna)

---

##  Vulnerabilidades Web

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Remote Code Execution (RCE)
- Server-Side Request Forgery (SSRF)
- Directory Traversal
- CSRF, Insecure Deserialization, LFI/RFI

### Herramientas de explotación Web
- `Burp Suite`
- `SQLmap`
- `XSStrike`
- `WFuzz` / `ffuf`
- `Nikto`
- `OWASP ZAP`
- `dirsearch`

---

## Descarga nuestra maquina virtual
- [Descargala aqui](https://soysena-my.sharepoint.com/:u:/g/personal/andres_velez99_soy_sena_edu_co/EWv8rcU5M-FMoeV6zk_-QxABOfTfrPLK6bMnfkrWJGwKDQ?e=7BhsKj)

---

## Requisitos y Herramientas
- **Linux:** Kali Linux, ParrotOS.
- **Active Directory:** Windows Server 2016/2019, BloodHound, Mimikatz.
- **AWS:** AWS CLI.

##  Recursos y Referencias
- [HackTricks](https://book.hacktricks.xyz/)

---

## Sitios web para aprender a resolver CTFs

- [Hack The Box](https://www.hackthebox.com/)
- [TryHackMe](https://tryhackme.com/)
- [Root-Me](https://www.root-me.org/)
- [CTFtime](https://ctftime.org/)
- [PicoCTF](https://picoctf.org/)
- [OverTheWire](https://overthewire.org/wargames/)

---

## Sitios web de documentación de vulnerabilidades

- [Exploit-DB](https://www.exploit-db.com/)
- [Mitre CVE](https://cve.mitre.org/)
- [NVD](https://nvd.nist.gov/)
- [Rapid7 Vulnerability DB](https://www.rapid7.com/db/)
- [PacketStorm](https://packetstormsecurity.com/)

---


⚠️ Este repositorio es solo para fines educativos y de aprendizaje. El uso indebido de estas técnicas es ilegal.

