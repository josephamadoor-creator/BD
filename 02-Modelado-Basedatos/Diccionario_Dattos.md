## Diccionario de Datos de la base de datos de Control Escolar 

1. Informacion General 
 Elemento  Valor 
 :---  :---

 Proyecto  Control Escolar 

 Version  1.0 

 Fecha  Junio 2026

 Elaboro  Joseph Amador 

 SGBD  SQLServer 

---
2. Descripcion del sistema de base de datos 

El sistema administra:
- Carreras
- Alumnos 
- Profesores 
- Materias 
- Grupos
- Inscripciones 

Permite controlar la ooferta academica y las inscripcion de estudiantes 

3. Catalogo de Restricciones utilizadas 
 Codigo  Significado 
 :---  :---
 PK Primary Key 
 FK Foreign Key 
 NN NOT NULL
 UQ UNIQUE 
 AI Auto Increment 
 CK Check 
 DF Default 

4. Diccionario de Datos 

## Tabla: Carrera

**Descripcion**

| Campo | Tipo | Longitud | Restricciones | Descripcion  |
| --------- | --------- | --------- | --------- | --------- |
| id_carrera  | INT  | - | PK,AI,NN | Identificador unico de la carrera  |
| nombre | VARCHAR  | 100 | UQ,NN  | Nombre de la carrera  |
| duracion_cuatrimestre b | VARCHAR  | 100 | UQ,NN  | Nombre de la carrera  |

---
## Tabla: Alumno

**Descripcion**




| Campo | Tipo | Longitud | Restricciones | Descripcion  |
| --------- | --------- | --------- | --------- | --------- |
| id_alumno | INT  | - | PK,AI,NN | Identificador unico del alumno  |
| matricula| VARCHAR  | 10 | UQ,NN  | Matricula Institucional  |
| nombre | VARCHAR  | 30 | NN  | nomnbre del alumno |
| apellido_paterno | VARCHAR  | 50 | NN  | Apellido Paterno |
| apellido_materno | VARCHAR  | 50 | NULL  | apellido Materno |
| correo | VARCHAR  | 100 | UQ,NN  | Correo Electronico |
| fecha_naci | VARCHAR  | DATE | -  | Fecha de Nacimiento |
| id_carrera | INT  | - | FK, NN  | Carrera a la que pertenece |

---
5. Relaciones en la bd 

| Relacion | Cardinalidad | Descripcion |
| :--- | :--- | :--- |
| carrera - alumno | 1:N | Una carrera tiene muchos alumnos |
| carrera - materia| 1:N | Una carrera tiene muchos alumnos |
| profesor - grupo | 1:N | Una carrera tiene muchos alumnos |
| materia - grupo | 1:N | Una carrera tiene muchos alumnos |
| alumno - grupo | 1:N | Una carrera tiene muchos alumnos |
| grupo - inscripcion| 1:N | Una carrera tiene muchos alumnos |

6. Materias de clase foranea 

| TABLA | CAMPO FK | REFERENCIA |
| :--- | :--- | :--- |
| Alumno      | id_carrera  | Carrera(id_carrera)   |
| Materia     | id_carrera  | Carrera(id_carrera)   |
| Grupo       | id_profesor | Profesor(id_profesor) |
| Grupo       | id_materia  | Materia(id_materia)   |
| Inscripcion | id_alumno   | Alumno(id_alumno)     |
| Inscripcion | id_grupo    | Grupo(id_grupo)       |

## 7. Integridad Referencial

| Código | Regla |
|--------|-------|
| IR-01 | No se puede registrar un alumno con una carrera inexistente |
| IR-02 | No se puede crear un grupo para una materia inexistente |
| IR-03 | No se puede crear un grupo para un profesor inexistente |
| IR-04 | No se puede inscribir un alumno en un grupo inexistente |
| IR-05 | No se puede eliminar una carrera que tenga alumnos asociados sin antes reasignarlos o eliminarlos |

## 8. Reglas del Negocio

| Código | Regla |
|--------|-------|
| RN-01 | Un alumno pertenece a una sola carrera |
| RN-02 | Una carrera puede tener muchos alumnos |
| RN-03 | Una carrera puede tener varias materias |
| RN-04 | Un profesor puede impartir varios grupos |
| RN-05 | Un grupo solo puede tener un profesor asignado |
| RN-06 | La calificación debe estar entre 0.0 y 10.0 |



