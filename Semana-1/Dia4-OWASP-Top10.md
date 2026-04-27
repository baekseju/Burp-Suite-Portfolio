# Día 4 – OWASP Top 10

## ¿Qué es OWASP?
Organización mundial de seguridad que publica
la lista de las 10 vulnerabilidades más críticas
de aplicaciones web.

## Mi resumen personal

### A01 – Broken Access Control
- **En una frase:** Veo lo que no debería ver
- **Ejemplo:** Cambio user_id=1234 por user_id=5678
  y veo pedidos de otra persona
- **Lo veré en:** Semana 4 (IDOR)

### A02 – Cryptographic Failures
- **En una frase:** Datos sin protección
- **Ejemplo:** Contraseñas sin encriptar
  o HTTP en vez de HTTPS

### A03 – Injection
- **En una frase:** Meto código y el servidor lo ejecuta
- **Ejemplo:** SQL Injection, XSS
- **Lo veré en:** Semana 2 y 3

### A04 – Insecure Design
- **En una frase:** Mal diseñado desde el principio
- **Ejemplo:** Banco sin límite de intentos de PIN

### A05 – Security Misconfiguration
- **En una frase:** Servidor mal configurado
- **Ejemplo:** Path Traversal
- **Estado:** ✅ Ya la practiqué

### A06 – Vulnerable Components
- **En una frase:** Software desactualizado con exploits
- **Ejemplo:** Server ATS/9.2.11 con vulnerabilidad conocida

### A07 – Authentication Failures
- **En una frase:** Login con fallas
- **Ejemplo:** Sin límite de intentos, fuerza bruta
- **Lo veré en:** Semana 3

### A08 – Data Integrity Failures
- **En una frase:** Sin verificación de datos
- **Ejemplo:** Actualizaciones sin firma digital

### A09 – Logging Failures
- **En una frase:** Sin registro de ataques
- **Ejemplo:** Atacante entra y sale sin dejar rastro

### A10 – SSRF
- **En una frase:** Fuerzo al servidor a hacer requests
- **Ejemplo:** Accedo a panel interno via el servidor


## Reflexión
No necesito memorizar definiciones exactas.
Necesito reconocer cada vulnerabilidad cuando
la veo en un lab y saber cómo atacarla.
