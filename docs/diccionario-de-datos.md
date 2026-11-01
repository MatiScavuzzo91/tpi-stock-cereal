# Diccionario de datos: qué cambia respecto de la Entrega 3

Al modelar el proceso en BPMN me di cuenta de que el diccionario de la Entrega 3 se quedaba corto, así que lo ajusto. Todo lo que no aparece acá sigue igual que en esa entrega.

| Entidad | Campo | Cambio | Motivo |
|---|---|---|---|
| Ubicación | `tipo` | Se agrega el valor Planta de acondicionamiento | La Entrega 1 la incluye como lugar del cereal, pero la Entrega 3 solo tenía Silo y Bolsón |
| Ubicación | `capacidad_kg` | Pasa a ser opcional para plantas | La capacidad de una planta externa no limita el stock propio |
| Destino | `tipo_destino` | Se agregan Traslado y Ajuste de inventario | Toda salida necesita un destino, también estas dos |
| Movimiento | `id_movimiento_vinculado` (Integer) | Campo nuevo, clave foránea a Movimiento, opcional | Une la salida y la entrada de un traslado |
| Movimiento | `vacia_ubicacion` (Boolean) | Campo nuevo | Dispara la comparación de stock de la meta de precisión |
| Movimiento | `autorizado_por` (String) | Campo nuevo, obligatorio en los ajustes | Deja constancia de qué jefatura lo autorizó |

Con esto resuelvo el supuesto que había dejado abierto en la Entrega 3: un traslado no es un tipo de movimiento propio, sino una salida y una entrada vinculadas. Un ajuste por faltante se registra como salida y uno por sobrante como entrada, siempre con el motivo en `observaciones`.
