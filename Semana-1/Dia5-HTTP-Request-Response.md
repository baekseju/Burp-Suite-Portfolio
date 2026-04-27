# Día 5 – HTTP Request/Response Handling

## ¿Qué aprendí?
- Anatomía completa de una REQUEST y RESPONSE
- Métodos HTTP: GET, POST, PUT, DELETE
- Códigos de respuesta y su significado
- Cómo el servidor confía en datos del cliente
- Ejecuté ataque: Excessive Trust in Client-Side Controls

## Anatomía de una REQUEST
| Parte | Descripción |
|-------|-------------|
| Método | GET, POST, PUT, DELETE |
| Ruta | URL + parámetros |
| Headers | Metadatos de la petición |
| Body | Datos enviados (solo POST) |

## Códigos de respuesta importantes
| Código | Significado | Para pentester |
|--------|-------------|----------------|
| 200 | OK | Todo normal |
| 302 | Redirección | Manipulable |
| 403 | Prohibido | Intenta bypassear |
| 404 | No encontrado | No existe |
| 500 | Error servidor | Muy interesante |

## Lab completado

### Excessive Trust in Client-Side Controls ✅
- **Vulnerabilidad:** A04 Insecure Design
- **Qué hice:** Modifiqué price=133700 a price=1
- **Resultado:** Compré jacket de $1337 por $0.01
- **Lección:** El servidor nunca debe confiar
  en datos que vienen del cliente

## Reflexión
El servidor confió ciegamente en el precio
que yo envié desde el navegador. En una tienda
real esto causaría pérdidas millonarias.
Los precios siempre deben calcularse en el
servidor, nunca en el cliente.
