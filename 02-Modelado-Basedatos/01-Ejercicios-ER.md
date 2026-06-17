# EJERCICIOS MODELADO E -R
---

1. Ejercicio 1

En un hospital se registra informacion de sus pacientes 

## De cada paciente se desea alamacenar:
---
- Algo que lo identifique 
- Nombre
- Fecha de nacimiento 

## De un expediente medico se almacena 
---
- Numero de Expediente

- Fecha de Aperuta

- Tipo de Sangre

## Reglas del Negocio 
---

## 2. Ejercicio 2

Una universidad administra:

- profesores 

- cursos 

> De cada profesor se alamcena:

- Clave profersor 

- Nombre

- Especialidad 

>De cada curso se almacena:

- Identificacion del Cuso

- Nombre del curso 

- Creditos 
---
## reglas del Negocio 
---
1. Puede impartir varios cursos 

2. Un curso solamente puede ser impartido por un profesor 

3. Puede existir un profesor que actualmente no imparta cursos

4. Todo curso todo debe ser asignado a un profesor

Se debe realizar lo siguiente:

- entidades

- Identificar la Relacion **IMPARTE**

- Detrminar la participacion 


---
## 3. Ejercicio 3

Una escuela administra alumnos y materias 

> De cada alumno se almacena:
 - Matricula 
 - Nombre 
 - Semestre 
 - Grupo 

> De cada materia se almacena:
 - Clave de la materia 
 - Nombre de la materia 
 - Creditos 

 ## - Reglas de la Escuela
 - Un alumno puede incribirse a varias materias 
 - Una materia puede tener muchos alumnos inscritos 
 - Puede existir una materia sin alumnos inscritos 
 - Todo alumno debe estar inscrito en al menos una materia 
 - De cada inscripcion se debe almacenar:
     - Fecha de inscripcion 
    - Calificacion final 
---
### 4. Una empresa encargada de realizar venta de productos:
> De cada cliente se almacena:
   - Numero de cliente que lo identifique
   - Y su nombre de cliente el cual es una persona moral
   - RFC 
> La empresa realiza pedidos los cuales almacena lo siguiente:
   - Numero de pedido
   - Fecha 
> La empresa tambien almacena productos de los cuales registra lo siguiente:
   - Numero del producto 
   - Nombre 
   - Precio
> Al realizar los pedidos deben registrar la cantidad de productos pedidos y precio 

## - Reglas 
- Un cliente puede realizar muchos pedidos 
- Cada pedido pertenece a un solo cliente
- Un pedido puede contener varios productos 
- Un producto puede aparecer en muchos pedidos 
- Un pedido debe contener al menos un producto
- Un producto puede no haber  sido vendido
- El detalle de pedido no existe sin pedido 
-  El detalle de pedido no existe sin producto
-  El detalle almacen cantidadd y precio de vent