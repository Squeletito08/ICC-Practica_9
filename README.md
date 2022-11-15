Introducción a Ciencias de la Computación
=========================================

Práctica 9: Interfaces gráficas
-------------------------------

### Fecha de entrega: martes 31 de mayo, 2022

Deben agregarle una interfaz gráfica con
[JavaFX](https://docs.oracle.com/javafx/2/get_started/jfxpub-get_started.htm) a
su base de datos de estudiantes.

![Interfaz gráfica](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/curso/-/wikis/uploads/f186fc2103325b56856959494cac5279/Screenshot_from_2022-11-15_01-34-05.png)

Esto implicará cambiar las propiedades de
[Estudiante](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/Estudiante.java),
a propiedades de JavaFX para poder agregar escuchas que reaccionen cuando
cambien su valor.

De la misma manera, deben modificar
[BaseDeDatos](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/BaseDeDatos.java),
para que se le puedan agregar escuchas instancias de
[EscuchaBaseDeDatos](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/EscuchaBaseDeDatos.java),
que reaccionen cuando la base de datos sea modificada; los escuchas reaccionarán
a eventos determinados en la enumeración
[EventoBaseDeDatos](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/EventoBaseDeDatos.java).

También deben completar *algunos* métodos de los controladores y clases
auxiliares de la interfaz gráfica, en el paquete
[igu](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/igu/).
Noten que estos métodos **no** tienen pruebas unitarias.

Una vez que hayan terminado sus clases, deben compilar al hacer:

```
$ mvn compile
```

No debe haber **ninguna** advertencia al compilar; si su práctica muestra
advertencias al compilar, se considerará como si no compilara.

También deben pasar todas sus pruebas unitarias al hacer:

```
$ mvn test
```

Por último, se debe ejecutar correctamente el programa escrito en la clase
[Practica9](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/src/main/java/mx/unam/ciencias/icc/Practica9.java)
al hacer:

```
$ mvn install
...
$ mvn -q exec:java \
      -f pom.xml   \
      -Dexec.mainClass=mx.unam.ciencias.icc.Practica9
```

Si no quieren teclear todo el comando, pueden usar el *script*
[`bin/practica9`](https://aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9/-/blob/main/bin/practica9)
para ejectuar el programa:

```
$ mvn install
...
$ ./bin/practica9
```

Los únicos archivos que deben modificar son:

* `Arreglos.java`,
* `BaseDeDatos.java`,
* `BaseDeDatosEstudiantes.java`,
* `CampoEstudiante.java`,
* `Estudiante.java`,
* `Lista.java`,
* `igu/ControladorFormaBusquedaEstudiantes.java`,
* `igu/ControladorFormaEstudiante.java`,
* `igu/ControladorForma.java`,
* `igu/ControladorInterfazEstudiantes.java`,
* `igu/ControladorTablaEstudiantes.java`,
* `igu/EntradaVerificable.java` y
* `igu/FabricaFormatoCelda.java`.

*No deben modificar de ninguna manera ninguno de los otros archivos de la práctica*.

### Repositorio

Pueden clonar la práctica con el siguiente comando:

```
$ git clone https://canek@aztlan.fciencias.unam.mx/gitlab/2023-1-icc/practica9.git
```

### Documentación

La documentación generada por JavaDoc la pueden consultar aquí:

[Documentación generada por JavaDoc para la práctica
9](https://aztlan.fciencias.unam.mx/~canek/2023-1-icc/practica9/apidocs/index.html)
