# Bandit Lab - OverTheWire

## Descripción
Este laboratorio introduce a los estudiantes al uso avanzado de la línea de comandos en sistemas Linux y al flujo de trabajo con Git y GitHub, utilizando una dinámica de retos progresivos inspirados en el wargame Bandit de OverTheWire.

Los estudiantes deberán resolver desafíos reales de línea de comandos, documentar cada paso de su proceso y versionar su progreso utilizando commits atómicos, simulando un entorno profesional de trabajo técnico.

**Sitio oficial del juego:** [https://overthewire.org/wargames/bandit/](https://overthewire.org/wargames/bandit/)

## Objetivo
Lograr alcanzar el nivel 10 o superior de Bandit para obtener la nota completa, demostrando dominio de:
- Navegación y manipulación de archivos/directorios desde la CLI
- Uso de comandos Unix esenciales
- Uso correcto de Git y GitHub exclusivamente desde la línea de comandos
- Documentación técnica clara y progresiva

## Acceso al Servidor
- **Usuario inicial:** bandit0
- **Contraseña inicial:** bandit0
- **Servidor:** bandit.labs.overthewire.org
- **Puerto:** 2220
- **Comando de conexión:** `ssh bandit0@bandit.labs.overthewire.org -p 2220`

---

## Progreso de Niveles

### Bandit Level 0 → Level 1
**Objetivo:**  
Encontrar la contraseña para el siguiente nivel en el archivo `readme` ubicado en el directorio home.

**Comandos utilizados:**
```bash
ls
cat readme
```

**Explicación:**  
Se listó el contenido del directorio home con `ls` para identificar los archivos presentes. Luego se utilizó `cat readme` para leer el contenido del archivo que contenía la contraseña del siguiente nivel.

**Contraseña obtenida:**  
`ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
