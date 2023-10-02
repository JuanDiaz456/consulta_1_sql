# consulta_1_sql
# Introduccion a las consultas a una BD usando el lenguaje SQL

## Base de datos: Ventas
## Tabla: Cliente

![Tabla Cliente](tabla_Cliente.png "Tabla Cliente")

## Instruccion SELECT
- permite seleccionar datos de una tabla
- su formto es: `SELECT campos_tabla FROM nombre tabla``

### consulta No. 1 
1. para visualizar toda la informacion que contiene la tabla cliente se puede incluir con la instruccio SELECT el caracter **\***  caa uno de los campos de la tabla.

- `SELECT * FROM Cliente`
![Tabla Cliente](ejem1.png "Tabla Cliente")

- `SELECT identificacion, nombre, apellidos, 
direccion, telefono, ciudad_nac, fecha_nac FROM Cliente`
![Tabla Cliente](ejem2.png "Tabla Cliente")

### consulta No. 2

2. para visualizar solamente la identificacion del cliente:`SELECT identificacion FROM Cliente`
![Tabla Cliente](ejem3.png "Tabla Cliente")

### consulta No. 3

3. si se desea obtener los registros cuya identificacion sea ayor o igual a 150, se debe utilizar la clausula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * FROM Cliente WHERE identificacion>=150`
![Tabla Cliente](ejem5.png "Tabla Cliente")

### consulta No. 4

4. se desea obtener los registros cuyos apellidos sean vanegas o Celina, se debe utilizar el operador `IN` que especifica los registros que se requieren visualizar en una tabla

`SELECT apellidos FROM Cliente WHERE apellidos IN('Vanegas', 'Cetina') `

![Tabla Cliente](ejem4.png "Tabla Cliente")
![Tabla Cliente](ejem7.png "Tabla Cliente")

o se puede utilizar el operador `OR`

`SELECT apellidos FROM Cliente WHERE apellidos = 'Vanegas' OR apellidos = 'Cetina' `

![Tabla Cliente](ejem6.png "Tabla Cliente")

### consulta No. 5

5. se desea obtener los registros cuya identificacion sea enor de 110 y la ciudad sea cali, se debe utilizar el operador `AND`

`SELECT * FROM Cliente WHERE identificacion<=110 AND ciudad_nac ='Cali'`
![Tabla Cliente](ejem8.png "Tabla Cliente")