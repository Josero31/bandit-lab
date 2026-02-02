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

---

### Bandit Level 1 → Level 2
**Objetivo:**  
Leer la contraseña del siguiente nivel almacenada en un archivo llamado `-` en el directorio home.

**Comandos utilizados:**
```bash
ls
cat ./-
```

**Explicación:**  
El archivo tiene el nombre especial `-` que puede ser interpretado como un argumento por la terminal. Para leerlo correctamente, se debe especificar la ruta relativa usando `./` antes del nombre del archivo, de manera que el comando `cat` lo interprete como un archivo y no como una opción.

**Contraseña obtenida:**  
`263JGJPfgU6LtdEvgfWU1XP5yac29mFx`

---

### Bandit Level 2 → Level 3
**Objetivo:**  
Leer la contraseña del siguiente nivel almacenada en un archivo llamado `spaces in this filename` en el directorio home.

**Comandos utilizados:**
```bash
ls
cat spaces\ in\ this\ filename
```

**Explicación:**  
El nombre del archivo contiene espacios, por lo que se debe usar el carácter de escape `\` antes de cada espacio para que la terminal interprete el nombre completo como un único argumento. Alternativamente, se pueden usar comillas: `cat "spaces in this filename"`.

**Contraseña obtenida:**  
`MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

---

### Bandit Level 3 → Level 4
**Objetivo:**  
Encontrar la contraseña del siguiente nivel que está almacenada en un archivo oculto dentro del directorio `inhere`.

**Comandos utilizados:**
```bash
cd inhere
ls -la
cat ...Hiding-From-You
```

**Explicación:**  
Se navegó al directorio `inhere` usando `cd`. Los archivos ocultos en Linux comienzan con un punto (`.`), por lo que se usó `ls -la` para listar todos los archivos incluidos los ocultos. El archivo `...Hiding-From-You` fue identificado y leído con `cat`.

**Contraseña obtenida:**  
`2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

---

### Bandit Level 4 → Level 5
**Objetivo:**  
Encontrar la contraseña del siguiente nivel que está almacenada en el único archivo legible por humanos dentro del directorio `inhere`.

**Comandos utilizados:**
```bash
cd inhere
file ./*
cat ./-file07
```

**Explicación:**  
Dentro del directorio `inhere` hay múltiples archivos. Se usó el comando `file ./*` para identificar el tipo de cada archivo. La mayoría contenían datos binarios, pero `-file07` fue identificado como texto ASCII. Se leyó su contenido con `cat ./-file07` para obtener la contraseña.

**Contraseña obtenida:**  
`4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`
