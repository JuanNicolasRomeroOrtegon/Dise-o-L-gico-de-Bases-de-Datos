# Diseño Lógico de Bases de Datos

Se presenta un resumen sobre los temas propuestos en el video de la **Universidad Politécnica de Valencia**, todo esto apoyándonos del **modelo relacional** para las bases de datos.

En el video se presenta primeramente un **enunciado** (problema a resolver) , el **diagrama entidad relación** (modelación de tablas) y el **diseño lógico** (esquema definitivo) cuyo objetivo es darle una solución al problema. 

Tenemos que tener presente que el **diseño lógico** se basa en un **modelo de datos** (tecnología para organizar la información).

Recordemos que un **esquema conceptual** se basa en entender los datos que necesitamos almacenar (es un primer paso para el modelado), mientras que el **esquema lógico** es la traducción de lo anterior a una **estructura de bases de datos real** con su debida implementación.

Si el **diagrama de entidad relación** es correcto a través de una serie de **reglas** obtendremos el **esquema lógico** (**Estructura definitiva de las tablas** y como estas se conectan), cuya función es indicar la estructura que tendrá la información.

---

## REGLAS A SEGUIR:

* Cada **entidad** del esquema conceptual es una **tabla** del esquema lógico. Además, los **atributos** de la entidad constituyen las **columnas** del esquema lógico.
* Las **relaciones n:n** (muchos a muchos) se modelan con una **tabla nueva**.
* Las **relaciones 1:n** no se deben implementar en una tabla nueva. En estas relaciones se debe añadir a la tabla que tiene la **relación muchos (N)** un nuevo atributo que apunta a la otra tabla con su **clave principal** entre paréntesis, este atributo se especifica como **clave ajena**.

### Se definen:

* **Clave Principal (Primary Key):** son atributos clave de la tabla actual.
* **Clave Ajena (Foreign Key):** sirven para exigir un **vínculo** entre los datos de dos tablas, es una referencia en una tabla que apunta a la **Primary Key** de otra.

---

## TABLA "AUXILIAR" PARA N:N

* Ayuda a definir la **relación muchos a muchos**, tiene atributos, dentro de los cuales se destacan la **clave primaria** de cada una de las entidades a las cuales se les está modelando la relación muchos a muchos, si las claves primarias tienen el mismo nombre, estas deben modificarse levemente para indicar de qué tabla hacen parte originalmente.
* Cuando esta tabla tiene un **atributo importante** que modele la relación muchos a muchos es importante añadirlo (Como la cantidad de veces que ocurre la relación).
* Su **clave primaria** es una **clave primaria compuesta** de las claves primarias de las tablas a las cuales les estamos haciendo la relación muchos a muchos.
* Cada **atributo clave** que ha sido **"heredado"** de las otras dos tablas se convierte en **clave ajena** que apunta a la entidad correspondiente y al atributo clave correspondiente original.

---

## CONCLUSIONES:

* Las **claves ajenas** sirven para **conectar** la información de una tabla con la información de otra.
* Gracias al **diseño lógico** obtenemos una descripción usando el **modelo relacional**.
* Obtenemos **relaciones** que concuerdan con la descripción del problema descrito.
* La información queda **ordenada**.
