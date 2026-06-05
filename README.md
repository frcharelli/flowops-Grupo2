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

## Instrucciones iniciales de ejecución
Este proyecto requiere el uso de Docker y Docker Compose para garantizar la consistencia del entorno de desarrollo entre los integrantes del equipo.

### Prerrequisitos
- Docker Desktop instalado.
- Git instalado.

### 1. Clonar el repositorio y preparar el entorno
Ejecutar los siguientes comandos en la terminal para descargar el proyecto y asegurar la creación de la estructura base de directorios:
git clone https://github.com/frcharelli/flowops-Grupo2.git

# Crear directorios locales para la persistencia de datos NoSQL
mkdir -p data/mongodb data/redis data/cassandra

### 2. Levantar la infraestructura NoSQL
Una vez configurado el archivo docker-compose.yml con las imágenes oficiales correspondientes a cada modelo candidato, iniciar los servicios en segundo plano mediante el comando:
docker compose up -d
Para verificar el estado y correcto funcionamiento de los contenedores, ejecutar:
docker compose ps

### 3. Comandos de mantenimiento y control
- Ver el historial de logs del entorno: docker compose logs -f
- Detener los servicios sin borrar los datos guardados: docker compose stop
- Apagar y remover los contenedores liberando los puertos: docker compose down