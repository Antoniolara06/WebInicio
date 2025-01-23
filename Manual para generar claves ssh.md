# Manual para generar claves SSH

## Generar una nueva clave SSH

### 1º abrimos Git bash.

### 2º Pegamos la siguiente línea de texto sustituyendo el email por el nuesto.
```bash
ssh-keygen -t ed25519 -C "tu_email@ejemplo.com"
```
#### Esto nos creara una nueva clave SSH.

### 3º Cuando se pida creamos una contraseña segura
```bash
> Enter passphrase (No ponemos nada para no crear contraseña): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
## Agregar tu clave SSH al ssh-agent

### 1º En una ventana de PowerShell con privilegios del adminstrador iniciamos el ssh-agent

```bash
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```
### 2º En una ventana del terminal agregamos la clave privada SSH al ssh-agent
```bash
ssh-add c:/Users/Nombre_Usuario/.ssh/id_ed25519
```
### 3º Agrega la clave pública de SSH a tu cuenta en GitHub

## Agregar un clave SSH nueva a tu cuenta

### 1º Copiamos el contenido de la llave SSH publica al portapapeles
```bash
cat /c/Users/YOU/.ssh/id_ed25519.pub
```
## En nuesto GitHub

### 1º Accedemos a los ajustes de nuestra cuenta de GitHub

### 2º Entramos al apartado de "SSH and GPG keys"

### 3º Le damos click a "New SSH key"

### 4º Ponemos el titulo y introducimos una informacion descriptiva para la clave

### 5º Seleccionamos que el tipo de clave sea de autentificación

### 6º En el campo "Key" pegamos la clave que tenemos en el portapapeles

### 7º Agregamos la clave SSH

## 8º Si se solicita, confirmamos la contraseña en GitHub