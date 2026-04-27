# Día 3 – Path Traversal Labs

## ¿Qué aprendí?
- Usar el Repeater a fondo
- Diferencia entre ruta relativa y ruta absoluta
- Cómo los servidores intentan bloquear ataques
- Cómo bypassear protecciones del servidor

## Conceptos clave
| Concepto | Definición |
|----------|------------|
| Ruta relativa | Navegar usando ../ desde ubicación actual |
| Ruta absoluta | Ir directo a la ruta completa /etc/passwd |
| Bypass | Saltarse una protección del servidor |
| /bin/bash | Usuario que puede iniciar sesión |
| nologin | Usuario que NO puede iniciar sesión |

## Labs completados

### Lab 1 - File path traversal, simple case ✅
- **Técnica:** filename=../../../etc/passwd
- **Resultado:** Obtuve lista completa de usuarios

### Lab 2 - Path traversal sequences blocked ✅
- **Técnica:** filename=/etc/passwd
- **Resultado:** Obtuve lista completa de usuarios
- **Diferencia:** El servidor bloqueaba ../ pero 
  no validaba rutas absolutas

## Información obtenida en Lab 2
| Dato | Valor |
|------|-------|
| Usuarios reales | peter, carlos, user, elmer |
| Base de datos | MySQL, PostgreSQL, MongoDB |
| Servidor web | www-data (Apache) |

## Reflexión
Aprendí que si una técnica de ataque no funciona,
siempre hay que probar variaciones. Los servidores
pueden bloquear ../ pero olvidarse de validar
rutas absolutas como /etc/passwd.
