# MRI-IngDatos2
# FlowOps TPO Grupo 2
## Integrantes
- Barbera Stark, Santiago
- Charelli, Franco
- Sanchez, Santiago Agustín
## Proceso elegido
Solicitud de vacaciones
## Descripción del problema
Permite a los empleados solicitar días de vacaciones de forma ordenada,
asegurando que cada solicitud pase por las aprobaciones necesarias 
antes de confirmarse.
## Primer flujo BPM
START → Formulario → Validación de días → Revisión Supervisor 
→ Revisión RRHH → Notificación → END
## Modelos NoSQL candidatos
- Definición de procesos: Documental
- Estado actual de instancias: Clave-valor
- Historial de eventos: Columnar/tabular
## Decisiones Pendientes
- **Selección del motor NoSQL:** Elección definitiva entre MongoDB, Redis o Cassandra (pendiente de profundizar en cada motor específico).
- **Diseño de datos:** Definición de esquemas internos e índices según el motor seleccionado.
- **Arquitectura distribuida:** Configuración de consistencia y particionamiento de datos (a desarrollar en el módulo de sistemas distribuidos).
- **Conectividad:** Implementación de la conexión desde la aplicación principal en fases posteriores.
- **Infraestructura y Despliegue:** Configuración de Docker y levantamiento de servicios (pendiente de estandarizar la instalación en el equipo).
- **Validación:** Definición de métricas de rendimiento y ejecución de *benchmarking* hacia el final de la cursada.
