# Plan de Pruebas - CR-004

## Casos mínimos 
- TC-AUTH-21: Login emite token con expiración de 1h.
- TC-AUTH-22: Token válido permite acceso a endpoint protegido.
- TC-AUTH-23: Token expirado devuelve 401 de forma consistente.
- TC-AUTH-24: Token firmado con llave anterior valida durante periodo de gracia.
- TC-AUTH-25: Token firmado con llave nueva valida correctamente.
- TC-AUTH-26: Sesión >1h: el cliente se recupera sin perder el flujo.

## Evidencia esperada
- Checklist marcado en el PR.
- Captura Postman o logs 
