# Día 1 – Instalación y Configuración de Burp Suite

## ¿Qué aprendí?
- Instalar y configurar Burp Suite Community Edition
- Configurar Firefox como proxy (127.0.0.1:8080)
- Instalar certificado de Burp en Firefox
- Interceptar requests con Forward y Drop
- Explorar el HTTP History

## Conceptos clave
| Concepto | Definición |
|----------|------------|
| Proxy | Intermediario entre navegador y servidor |
| Request | Lo que el navegador envía al servidor |
| Response | Lo que el servidor responde |
| Forward | Dejar pasar la request |
| Drop | Descartar la request |
| HTTP History | Registro de todo el tráfico capturado |

## Práctica realizada
- Intercepté requests reales de Wikipedia y YouTube
- Analicé headers, cookies y códigos de respuesta
- Descubrí que CNN detectó mi ubicación en Costa Rica
  usando solo mi dirección IP

## Reflexión
Aprendí que todo el tráfico entre el navegador 
y el servidor puede ser interceptado y analizado
con Burp Suite.
