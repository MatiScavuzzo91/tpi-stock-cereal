# Indicadores de control y estándares de desempeño

Para cada indicador sigo la misma idea: fijo un estándar, mido, comparo y corrijo. En la columna **Origen** anoto de dónde sale el estándar: **E2** o **E3** si ya estaba en una entrega anterior, y **Propuesto** si es nuevo y todavía lo tengo que validar con las jefaturas.

| Código | Indicador | Medición | Estándar | Frecuencia | Responsable | Acción si no se cumple | Origen |
|---|---|---|---|---|---|---|---|
| IC-1 | Precisión del stock | \|saldo registrado al vaciar\| / total de entradas registradas × 100 | Hasta 0,5 % | Cada vaciado | Asistente; autoriza jefatura | Analizar el desvío y registrar un ajuste autorizado | E2 |
| IC-2 | Tiempo de respuesta | Consulta de stock con 5000 registros | Hasta 5 s | Pruebas (sem. 15-17) y cada versión | Desarrollador | Revisar índices y consultas | E2 |
| IC-3 | Tiempo de carga | Promedio de 20 cargas cronometradas | Menos de 20 s (base: 30-45 s) | Pruebas con usuarios (sem. 17) y fin de operación en paralelo | Desarrollador | Simplificar el formulario | E2 |
| IC-4 | Cumplimiento de hitos | Semana real menos semana planificada | H1 sem. 13, H2 sem. 20, H3 sem. 26 | Semanal | Desarrollador | Reprogramar y usar el colchón de las sem. 20-26 | E2 |
| IC-5 | Integridad de los registros | Salidas con destino y movimientos con `cargado_por` / total × 100 | 100 % | Semanal | Desarrollador | Corregir los registros y reforzar la validación | E3 |
| IC-6 | Conciliación con Excel | \|stock sistema − stock Excel\| / stock Excel × 100, por ubicación y cereal | Hasta 0,5 % | Semanal (sem. 20-26) | Asistente | Buscar el movimiento que origina la diferencia | Propuesto |
| IC-7 | Oportunidad de la carga | Movimientos cargados hasta 1 día hábil después del remito / total × 100 | Al menos 90 % | Mensual | Encargada de Administración | Revisar la circulación de los remitos | Propuesto |

## Cómo se puede auditar

- **Los datos:** los movimientos no se editan sin dejar rastro. Los campos `cargado_por` y `autorizado_por` indican quién registró y quién autorizó cada cosa.
- **Los cambios:** todo cambio entra por una rama y un Pull Request vinculado a un issue del tablero.
- **La evidencia:** cada medición de IC-1, IC-2 e IC-3 se anota en un issue, con la fecha, el valor y lo que se hizo al respecto.

Como el módulo todavía no está construido, IC-1, IC-2, IC-3, IC-5, IC-6 e IC-7 son estándares definidos pero todavía sin mediciones.
