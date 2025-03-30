# script_kiddie
Este repositorio está dedicado al aprendizaje y desarrollo de habilidades en el ámbito del hacking ético.
# Hacking & Cybersecurity Repository

Bienvenido a este repositorio dedicado al aprendizaje y práctica del hacking ético en diversas plataformas y entornos. Aquí encontrarás recursos, técnicas y guías sobre hacking en Linux, Active Directory y AWS.

## ✨ Contenido

- [Hacking en Linux](#hacking-en-linux)
  - [Post-explotación en Linux](#post-explotación-en-linux)
  - [Escalada de privilegios](#escalada-de-privilegios)
  - [Pivoting y Tunneling](#pivoting-y-tunneling)
  - [Bypassing de seguridad](#bypassing-de-seguridad)
- [Hacking en Active Directory](#hacking-en-active-directory)
  - [Enumeración en Active Directory](#enumeración-en-active-directory)
  - [Ataques de Kerberos](#ataques-de-kerberos)
  - [Escalada de privilegios en AD](#escalada-de-privilegios-en-ad)
  - [Persistence y Dominación](#persistence-y-dominación)
- [Hacking en AWS](#hacking-en-aws)
  - [Enumeración y reconocimiento](#enumeración-y-reconocimiento)
  - [Explotación de IAM](#explotación-de-iam)
  - [Persistencia en AWS](#persistencia-en-aws)
  - [Post-explotación](#post-explotación)

---

## 🔍 Hacking en Linux

### Post-explotación en Linux
- Técnicas para mantener el acceso en sistemas Linux comprometidos.
- Uso de herramientas como `chattr`, `crontab` y `systemd`.

### Escalada de privilegios
- Explotación de binarios con `SUID` y `sudo` mal configurados.
- Vulnerabilidades Kernel y explotación de `CVE` relevantes.

### Pivoting y Tunneling
- Configuración de `ProxyChains` y `SSH Tunneling`.
- Uso de `Chisel`, `Sshuttle` y `Metasploit` para pivoting.

### Bypassing de seguridad
- Evasión de antivirus y soluciones EDR.
- Uso de `LD_PRELOAD`, `ptrace` y `Syscall hooking`.

---

## 🛡️ Hacking en Active Directory

### Enumeración en Active Directory
- Uso de `BloodHound`, `ldapsearch` y `PowerView`.
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

## ☁️ Hacking en AWS

### Enumeración y reconocimiento
- Uso de `awscli`, `Pacu` y `CloudMapper`.
- Extracción de metadatos en EC2 (`IMDSv1 vs IMDSv2`).

### Explotación de IAM
- Extracción y abuso de credenciales en `AWS IAM`.
- Uso de `Lambda`, `EC2` y `S3` para acceso persistente.

### Persistencia en AWS
- Creación de backdoors en roles y políticas.
- Uso de `CloudTrail` para detección y evasión.

### Post-explotación
- Uso de `SSRF` para acceso a recursos internos.
- Persistencia en `AWS Organizations` y `AssumeRole`.

---

## ⚙️ Requisitos y Herramientas
- **Linux:** Kali Linux, ParrotOS, Ubuntu.
- **Active Directory:** Windows Server 2016/2019, BloodHound, Mimikatz.
- **AWS:** AWS CLI, Pacu, CloudMapper, ScoutSuite.

## 📚 Recursos y Referencias
- [HackTricks](https://book.hacktricks.xyz/)
- [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
- [Red Team Field Manual](https://www.amazon.com/Red-Team-Field-Manual-RTFM/dp/1494295504)

## ✅ Contribuciones
¡Las contribuciones son bienvenidas! Si quieres agregar contenido, abre un PR o un issue en este repositorio.

---

⚠️ **Disclaimer:** Este repositorio es solo para fines educativos y de aprendizaje. El uso indebido de estas técnicas es ilegal y no está respaldado por este proyecto.

