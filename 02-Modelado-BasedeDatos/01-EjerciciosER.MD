# Ejercicios del Modelo E-R 

## Ejercico 1.

Un hospital registra infomacion de sus paciantes:

> De cada paciante que almacena:
- numnero de paciente que lo 
identifica 
- Nombre 
- Fecha de Nacimiento 
> De cada expediente medico se 
almacena 
-Numero de expediente
- Fecha de Apertura 
- Tipo de Sangre 

>Reglas de Negocio 
1. Cada Paciente debe tener 
exactamente un expediente medico
2.Cada expediente Medico
pertenece a un unico paciente 
3. No pude existir un expediente sin paciente
4. no puede existir un paciente sin expediente

>Que se bede realizar:
- identidficar las entidaedes
- identiicar atributos 
- dibujar las relaciuon
- determinar la cardinalidad
- determinar la participacion de cada entidad

[Eqjercicio](../img/)

## Ejercicio 2.
Una Universidad administra profesores y cursos 

> De cada profesor se almacena:

- Numero de Profesor 
- Nombre 
- Especialidad

> De cada **Curso** se alamacena: 

- Numero de Curso 
- Nombre del curso 
- Credito 

> Reglas del Negocio 

1. Un profesor puede impartir varios cursos 
2. Un curso solamente puede ser impartido por un profesor
3. Puede existir un profesor que actualmente no imparta cursos 
4. Todo curso debe estar asignado a un profesor 

[Ejercicio2](../img/ER/Ejercicio)

## Ejercicio 3

Una escuela administra alumnos y materias 

> De cada **Alumno** se alamcena:

- Materia 
- Nombre
- Semestre 

> De cada **Materia** se almacena:

- Clave de la materia 
- Nombre de la materia 
- Creditos 

> Reglas del negocio

1. Un alumno puede inscribirse en varias materias 
2. Una materia puede tener muchos alumnos inscriptos 
3. Puede existir una materia sin alumnos inscriptos 
4. Todo alumno debe estar inscripto en al menos una materia 
5. De cada inscripcion se desea almacenar:
    -Fecha de inscripcion
    -Calificacion Final
Nota: a la relacion nombrarla **INSCRIBE**

[EJERCIO](JUIU)

## Ejercicio 4

Una empresa dedicada a las vetas al por mayor necesita registrar lo siguiente:

> Para los clientes:
- Nombre del Cliente 
- Nombre (el cual es una persona moral)

> Pedidos

- Numero de Pedido
- Fecha de Pedido

> Reglas del Negocio

1. Un cliente puede realizar muchos pedidos 
2. Cada pedido pertenece a un solo cliente
3. Un pedido contiene varios productos 
4. Un producto puede aparecer en muchos pedidos 
5. Un pedido debe contener al menos un producto
6. Un producto puede no haber sidop vendido 
7. El detalle del pedido no existe sin pedido
8. El detalle del pedido no existe sin producto 
9. El detalle almacena la cantidad vendida y el precio de venta 