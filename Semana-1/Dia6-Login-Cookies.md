# Día 6 – Login Interceptado + Cookies

## ¿Qué aprendí?
- Interceptar un formulario de login real
- Ver contraseñas en texto plano en Burp
- Qué son las cookies y cómo funcionan
- Username Enumeration
- Brute Force con el Intruder
- Diferencia entre HTTP/1.1 y HTTP/2

## ¿Qué son las Cookies?
Las cookies son como un brazalete que el servidor
te da después del login para recordar que ya
iniciaste sesión. Viajan en cada request automáticamente.

## Ataque realizado: Username Enumeration + Brute Force

### Paso 1 - Encontré el usuario válido
- El servidor respondía diferente según el usuario:
  - Usuario incorrecto: "Invalid username"
  - Usuario correcto: "Incorrect password"
- Usé el Intruder con lista de 101 usuarios
- Usuario encontrado: agenda ✅

### Paso 2 - Encontré la contraseña
- Usé el Intruder con lista de contraseñas
- La request con Status 302 reveló la contraseña
- Contraseña encontrada: monitoring ✅

## ¿Por qué funcionó?
| Falla del servidor | Consecuencia |
|-------------------|-------------|
| Mensajes de error diferentes | Revela si usuario existe |
| Sin límite de intentos | Permite fuerza bruta |
| Sin CAPTCHA | Ataque automatizable |

## Lab completado
- ✅ Username enumeration via different responses (Apprentice)

## Reflexión
Un servidor nunca debe revelar si el usuario
existe o no. El mensaje de error siempre debe
ser el mismo: "Usuario o contraseña incorrectos"
