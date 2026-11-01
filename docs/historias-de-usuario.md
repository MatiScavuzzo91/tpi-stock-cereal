# Historias de usuario

Las entregas anteriores no tenían historias de usuario formales, así que las armo acá a partir del objetivo y las metas de la Entrega 2 y de los puestos del organigrama de la Entrega 3. Las voy siguiendo en el tablero del proyecto.

## HU-01: Registrar un movimiento

**Como** asistente administrativo, **quiero** registrar cada entrada, salida o traslado de cereal a partir del remito o la planilla, **para** dejar de calcular las existencias a mano en Excel.

Cómo sé que está lista:

- Si falta un dato obligatorio, el sistema no deja cargar el movimiento y me dice cuál es.
- Una salida necesita un destino, y un traslado genera una salida y una entrada vinculadas.
- Si la salida supera el stock calculado, el sistema avisa de la diferencia y no la registra hasta que se verifique.
- Cargar un movimiento lleva menos de 20 segundos (es la meta de la Entrega 2; hoy toma entre 30 y 45).

## HU-02: Consultar el stock disponible

**Como** jefatura, **quiero** consultar el stock por ubicación y cereal, **para** decidir ventas y canjes sin comprometer el cereal destinado al consumo del tambo.

Cómo sé que está lista:

- El stock se calcula como entradas menos salidas, por ubicación y cereal.
- La consulta se puede filtrar por campaña.
- La molienda interna se descuenta del stock disponible.
- La consulta responde en 5 segundos o menos con 5000 registros por año.

## HU-03: Conciliar al vaciar una ubicación

**Como** asistente administrativo, **quiero** comparar el stock registrado con el físico cuando se vacía un silo o bolsón, **para** verificar que el desvío no supere el 0,5 % y escalar a la jefatura si lo supera.

Cómo sé que está lista:

- El sistema calcula el desvío cuando marco que un movimiento vacía la ubicación.
- Si el desvío es de hasta 0,5 %, la ubicación queda conciliada.
- Si es mayor, hace falta que una jefatura autorice el ajuste para poder registrarlo.
- Cada ajuste guarda quién lo cargó, quién lo autorizó y el motivo.
