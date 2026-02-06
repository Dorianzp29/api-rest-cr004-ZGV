# Análisis de Impacto y Riesgo - CR-004

## Impacto (Tabla 2 )
- Alcance: cambia. Afecta el manejo de sesión y a clientes externos.
- Tiempo: +1 a 2 días. Incluye ajuste, pruebas de integración y documentación.
- Costo: +. Horas Dev/QA/DevOps; sin licencias.
- Calidad: riesgo a QA/QC. Puede aumentar 401 “esperados”; requiere pruebas completas.
- Arquitectura: auth/JWT y gestión de llaves; consistencia entre nodos.
- Seguridad: afecta (mejora). Menor ventana de exposición y rotación controlada.
- Operación: despliegue por etapas y rollback definido.

## Matriz de riesgo (Tabla 3 )
1) Clientes no manejan expiración 1h y fallan con 401 (Prob: Media, Impacto: Alto).
   Mitigación: pruebas de integración + guía corta + monitoreo de 401.

2) Rotación mal aplicada invalida tokens en uso (Prob: Baja/Media, Impacto: Alto).
   Mitigación: periodo de gracia + uso de kid + checklist previo a producción.

3) Inconsistencia entre servidores (Prob: Media, Impacto: Alto).
   Mitigación: configuración centralizada + prueba multi-nodo + verificación en pipeline.
