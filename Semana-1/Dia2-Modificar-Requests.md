# Día 2 – Modificar Requests en Tiempo Real

## ¿Qué aprendí?
- Falsificar User-Agent para engañar al servidor
- Modificar parámetros en la URL
- Usar el Repeater por primera vez
- Entender códigos de respuesta HTTP
- Ejecutar mi primer ataque real: Path Traversal

## Conceptos clave
| Concepto | Definición |
|----------|------------|
| User-Agent | Identificación del navegador ante el servidor |
| Parámetro | Valor en la URL después del signo ? |
| Path Traversal | Acceder a archivos fuera del directorio permitido |
| ../ | Subir un nivel en la estructura de carpetas |
| Repeater | Herramienta para reenviar y modificar requests |

## Prácticas realizadas
- Falsifiqué User-Agent como iPhone y Google recibió
  versión móvil
- Falsifiqué User-Agent como GoogleBot en Facebook
  y recibí error 400
- Falsifiqué User-Agent como Internet Explorer en CNN
  y descubrí mi ubicación en las cookies
- Ejecuté Path Traversal y obtuve /etc/passwd del servidor

## Archivos obtenidos con Path Traversal
| Archivo | Resultado |
|---------|-----------|
| /etc/passwd | ✅ Lista de usuarios del sistema |
| /etc/hostname | ✅ Nombre del servidor |
| /proc/version | ✅ Linux kernel + IP interna + AWS |
| /etc/shadow | ❌ Acceso denegado |

## Lab completado
- ✅ File path traversal, simple case (Apprentice)

## Reflexión
Aprendí que ningún valor en una HTTP request 
es confiable porque puede ser modificado antes 
de llegar al servidor. Los servidores que no 
validan sus parámetros son vulnerables a ataques
como Path Traversal.
