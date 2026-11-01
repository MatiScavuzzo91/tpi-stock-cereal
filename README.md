# Módulo de stock de cereal

Documentación del Trabajo Práctico Integrador (TPI) de Organización Empresarial, de la Tecnicatura Universitaria en Programación a Distancia (UTN).

## Descripción del sistema

Es un módulo a medida para una empresa agrícola-ganadera, pensado para dejar atrás las planillas de Excel que hoy se cargan a mano para controlar el cereal. Registra entradas, salidas y traslados entre silos, bolsones y plantas de acondicionamiento, y calcula cuánto cereal hay en cada lugar, separando el que se vende o se canjea del que se consume en el tambo.

Por ahora el módulo está en etapa de análisis y diseño, así que este repositorio tiene solo la documentación y todavía no hay código.

## Tablero de gestión

[Backlog en GitHub Projects](https://github.com/users/MatiScavuzzo91/projects/1)

## Integrantes

- Matías Nicolás Scavuzzo (desarrollador único)

## Declaración de Uso de IA

Usé Claude (Anthropic), a través de Claude Code, como ayuda para armar esta entrega.

### Prompts utilizados y por qué los usé así

| Prompt o instrucción | Por qué lo usé así |
|---|---|
| "Acabo de descargar los lineamientos para la entrega 4 del TPI. Tenés las entregas anteriores para armar el 4to en función de las entregas anteriores siguiendo el mismo proyecto" | Le di las entregas anteriores como contexto para que el resultado siguiera el mismo caso y no saliera algo genérico. Como el pedido era amplio y le dejaba mucho librado, después revisé todo contra lo que pasa de verdad en la empresa. |
| Mis respuestas a sus preguntas sobre cómo llega el dato a Administración y cómo tratar los traslados | Eran datos y decisiones del proyecto que el modelo no podía conocer y que no tenía que inventar, así que las contesté yo. |

### Correcciones y decisiones mías

- El origen del dato (remito o planilla) lo aporté yo, porque no se podía deducir de las entregas anteriores.
- Entre las alternativas que se plantearon, elegí modelar los traslados como una salida y una entrada vinculadas.
- Le indiqué la cuenta de GitHub de la carrera para publicar el repositorio.

### Qué hay que tomar con cuidado

Claude redactó los borradores del BPMN, de las historias de usuario y de los indicadores. Los estándares marcados como "Propuesto" y la idea de que las jefaturas autoricen los ajustes son propuestas que todavía tengo que validar con la empresa. Soy responsable del contenido.
