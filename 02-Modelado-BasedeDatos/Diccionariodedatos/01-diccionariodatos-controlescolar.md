# Diccionario de Datos de la Base de Datos control Escolare 

1.  Informacion General 

| Elemento  | Valor  |
| :---  | :---  |
| Proyecto  | Control Escolar  |
| Version  | 1.0  |
| Fecha | Junio 2026 |
| Elaboro | Cristian Uriel Martinez Galindo |
| SGBD | SQLSERVER |

2. Descripcion de la base de Datos

El Base de Datos Administra:

- Carrera 
- Alumno
- Profesor
- Materia
- Grupo
- Inscripcion

Permite controlar la oferta academica y la inscripcion de estudiantes 

3. Catalogo de Retrcciones Utlizadas

| Catalogo  | significado  |
| :---  | :---  |
| PK   | Primary key  |
| FK   | Foreing key  |
| NN   | Not Null |
| UQ   | Unique |
| AI   | Autoincrement o Identity  |
| CK   | Check  |
| VDF  | Default | 

4. Diccionario de Datos 

**Tabla:** _carrera_

**Descripcion** 
Almacena las carreras ofertadas por la Universidad

| Campo | Tipo | Longitud | Restricciones | Descripcion |
| :--- | :--- | :--- | :--- | :--- |
| id_carrera | INT| - | PK, AI, NN | Identificador unico de la carrera |
| nombre | VARCHAR | 100 | UQ, NN | Nombre de la carrera |
| duracion_cuatrimestre | INT | - | NN, CK(>0)| Duracion en cuatrimestre| 

---

**Tabla:** _Alumno_

**Descripcion** 
Almacena la informacion de los estudiantes 

| Campo | Tipo | Longitud | Restricciones | Descripcion |
| :--- | :--- | :--- | :--- | :--- |
| id_alumno | INT| - | PK, AI, NN | Identificador del alumno|
| matricula | VARCHAR | 10 | UQ, NN | Matricula Institucional |
| nombre | VARCHAR | 50 | NN | Nombre del alumno| 
| apellido-paterno | VARCHAR | 50 | NULL | Apellido Paterno| 
| apellido-materno | VARCHAR | 50 | NULL | Apellido Materno|
| correo | VARCHAR | 100 | UQ, NULL | CORREO Institucional|
| fecha-nacimiento | DATE | - | NN | Fecha Nacimiento |
| id-carrera | INT | - | FK, NN | Carrera a la que pertenece |

---

TODO: Documentar las siguientes tablas 

5. Relaciones en Base de Datos 

| Relacion | Cardinalidad | Descripcion | 
| :--- | :--- | :--- | 
| carrera -> Alumno | 1:N | Una carrera tiene muchos alumnos | 
| carrera -> Materia | 1:N | Una carrera tiene muchas materias | 
| carrera -> Grupo | 1:N | Una profesor puede impartir en varios grupos | 
| materia -> Grupo | 1:N | Una materia puede abrirse en varios grupos |
| alumno -> Inscripcion | 1:N | Una alumno puede tener varias inscripciones |
| Grupo -> Inscripccion | 1:N | Una grupo puede tener muchos alumnos

6. Matriz de Clave Foraneas

| Tabla | Campo FK | Referencia | 
| :--- | :--- | :--- | 
| Alumno | id_carrera | carrera(id_carrera) | 
| Materia | id_carrera | carrera(id_carrera) | 
| Grupo | id_profesor | Profesor(id_profesor) | 
| Grupo | id_materia | Materia(id_materia)
| Inscripcion | id_alumno | Alumno(id_alumno) | 
| Inscripcion | id_grupo | Grupo(id_grupo) |  

7. Integridad Referencial 

| Clave | Regla |
| :--- | :--- |
| IR-01 | No se puede registrar un alumno con una carrera inexistenete |
| IR-02 | No se puede crear un grupo para una materia inexistente |
| IR-03 | No se puede crear un grupo para un profesor inexistente |

8. Reglas del negocio 

| Clave | Regla |
| :--- | :--- |
| RN-01 | Un alumno pertenece a una sola carrera |
| RN-02 | Una carrera puede tener muchos alumnos |
| RN-03 | Una carrera puede tener muchas materias|
| RN-04 | Un profesor puede impartir varios grupos |

9. Diagrama Relacional

