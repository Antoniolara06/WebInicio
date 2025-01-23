# Manual para generar claves SSH

## 1º abrimos Git bash.

## 2º Pegamos la siguiente línea de texto sustituyendo el email por el nuesto.
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
### Esto nos creara una nueva clave SSH.

## 3º Cuando se pida creamos una contrasela segura
```bash
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```