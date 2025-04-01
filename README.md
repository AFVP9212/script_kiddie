# script_kiddie
Este repositorio está dedicado al aprendizaje y desarrollo de habilidades en el ámbito del hacking ético.
# Hacking & Cybersecurity Repository

Bienvenido a este repositorio dedicado al aprendizaje y práctica del hacking ético en diversas plataformas y entornos. Aquí encontrarás recursos, técnicas y guías sobre hacking en Linux, Active Directory y AWS.

## Contenido

- [Hacking en Linux](#hacking-en-linux)
  - [Post-explotación en Linux](#post-explotación-en-linux)
  - [Escalada de privilegios](#escalada-de-privilegios)

- [Hacking en Active Directory](#hacking-en-active-directory)
  - [Enumeración en Active Directory](#enumeración-en-active-directory)
  - [Ataques de Kerberos](#ataques-de-kerberos)
  - [Escalada de privilegios en AD](#escalada-de-privilegios-en-ad)
  - [Persistence y Dominación](#persistence-y-dominación)

- [Hacking en AWS](#hacking-en-aws)
  - [Enumeración y reconocimiento](#enumeración-y-reconocimiento)
  - [Explotación de IAM](#explotación-de-iam)

---

## Hacking en Linux

### Post-explotación en Linux
- Técnicas para mantener el acceso en sistemas Linux comprometidos.

### Escalada de privilegios
- Explotación de binarios con `SUID` y `sudo` mal configurados.
- ```sudo -l ``` `sudo su`
- Vulnerabilidades Kernel y explotación de `CVE` relevantes.

---

## Hacking en Active Directory

### Enumeración en Active Directory
- Uso de `BloodHound` y `PowerView`.
- Extracción de usuarios, grupos y GPOs.

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

