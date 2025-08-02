# Training-Week-One-DDBB

📄 README - Sistema de Gestión de Citas Médicas 🏥
📁 Archivos Incluidos
DER.pdf
Contiene el Diagrama Entidad-Relación (DER) del sistema, que representa las entidades principales, sus atributos y relaciones lógicas.

ModeloRelacional.pdf
Contiene el Modelo Relacional, que muestra las tablas de la base de datos con sus respectivos campos y tipos de datos.

🧱 Descripción General
Este sistema está diseñado para gestionar las citas médicas del hospital Vida Sana, abarcando el registro de pacientes, médicos, diagnósticos y sus relaciones. Ambos documentos son parte del diseño de base de datos necesario para garantizar la integridad, trazabilidad y eficiencia del manejo de información médica.

📌 Entidades Principales
1. 👤 Paciente
Atributos:

id_paciente (PK)

nombre_completo

fecha_nacimiento

genero

telefono

correo

direccion

tipo_sangre / rh

2. 👨‍⚕️ Médico
Atributos:

id_medico (PK)

nombre_completo

especialidad

telefono

correo

años_experiencia / experiencia

salario

3. 🗓️ Cita
Atributos:

id_cita (PK)

fecha

hora / hora_cita

motivo_consulta / motivo_cita

estado / estado_cita

id_paciente (FK)

id_medico (FK)

Relaciones:

Un paciente puede solicitar muchas citas (1:N)

Un médico puede atender muchas citas (1:N)

4. 📋 Diagnóstico
Atributos:

id_diagnostico (PK)

descripcion

indicaciones

receta / formula

id_cita (FK)

Relación:

Cada cita tiene un único diagnóstico (1:1)

🔄 Correspondencia entre DER y Modelo Relacional
Entidad (DER)	Tabla (Relacional)
Paciente	paciente
Medico	medico
Cita	cita
Diagnóstico	diagnostico

🔗 Relaciones Clave
paciente (1) —— (N) cita

medico (1) —— (N) cita

cita (1) —— (1) diagnostico

✅ Consideraciones Técnicas
El modelo relacional usa tipos SQL estándar como int, varchar, date, decimal, text, time.

Las claves primarias están bien definidas para cada tabla.

Las claves foráneas aseguran la integridad referencial entre las entidades.
