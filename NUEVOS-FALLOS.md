# NUEVOS FALLOS

**Nota:** Para no reemplazar el fichero test de cada ejercicio, nuestro fichero de test acabará en 2 (p.e. `BisiestoTest2.java`).

___

## Ejercicio 1 - Bisiestos
- **Apartado 1.** Enlace de GitHub al código que contiene el fallo:
	- [Link al SUT](https://github.com/Onac8/nshandra_Practica-ISI/blob/master/pruebasIDM/Bisiestos/Bisiestos.java)
	- [Link al fichero de tests](https://github.com/Onac8/nshandra_Practica-ISI/commit/c81469432f40f4776711653486dd84d9d8e27dfb#diff-6441aefcf426fa02cbde5b2cd92ea543)
- **Apartados 2-3.** Descripción de fallos y adaptaciones de nuestros tests para probar el código del otro grupo:
	- Pasamos 6 tests. Nos sale 1 error:
		1. En `testForZeroYear`, ya que nosotros consideramos que el 0 no es bisiesto y ellos sí. Para que pase el test, hemos tenido que cambiar el `assertFalse` por un `assertTrue` al pasar como entrada el año 0 y comprobar que es bisiesto.
- **Apartado 4.** Enlace de GitHub a `BisiestoTest2.java` adaptado a su SUT:
	- [Link al fichero de tests modificado](https://github.com/Onac8/nshandra_Practica-ISI/commit/32a20048b68ed28fd4c5bc31eb6fbe1632a9b725#diff-6441aefcf426fa02cbde5b2cd92ea543)

## Ejercicio 2 - Romanos
- **Apartado 1.** Enlace de GitHub al código que contiene el fallo:
	- [Link al SUT](https://github.com/Onac8/nshandra_Practica-ISI/blob/master/pruebasIDM/RomanNumeral/RomanNumeral.java)
	- [Link al fichero de tests](https://github.com/Onac8/nshandra_Practica-ISI/commit/ec0d5624c7455844967017b5ca4589f3727975dd#diff-30b7fdaaeb3bd2f8d2876cb6616b53e6)
- **Apartados 2-3.**	Descripción de fallos y adaptaciones de nuestros tests para probar el código del otro grupo:
	- Pasamos 3 tests. Nos salen 2 errores:
		1. En `testForNoRoman`, salía error ya que ellos han optado por devolver `0` cuando la entrada es distinta de un caracter romano. Es por eso por lo que no se eleva ningún tipo de excepción, simplemente el método `convierte()` devuelve `0`. lo que hemos hecho para que pase el test es borrar la línea donde ponía que se esperaba una excepción de tipo `IllegalArgumentException` y hemos puesto un `assertTrue` comprobando que, efectivamente, se devuelve `0` cuando se pasa un número que no es romano.
		2. En `testForNullString` ocurre exactamente lo mismo que lo descrito anteriormente.
- **Apartado 4.** Enlace de GitHub a `RomanNumeralTest2.java` adaptado a su SUT:
	- [Link al fichero de tests modificado](https://github.com/Onac8/nshandra_Practica-ISI/commit/0333f3fdb0882ec323a44367807ea63a11437574#diff-2e09de0612f076984f73bcf8f4bc170d)

## Ejercicio 3 - Embotelladora
- **Apartado 1.** Enlace de GitHub al código que contiene el fallo:
	- [Link al SUT](https://github.com/Onac8/nshandra_Practica-ISI/blob/master/pruebasIDM/Embotelladora/Embotelladora.java)
	- [Link al fichero de tests](https://github.com/Onac8/nshandra_Practica-ISI/commit/7df9f7c2ab8bec97c3677ac2ee0a087416c5a31a)
- **Apartados 2-3.**	Descripción de fallos y adaptaciones de nuestros tests para probar el código del otro grupo:
	- Pasamos 13 tests. Nos salen 5 errores:
		1. En `testForNegativePequenas`, ya que nosotros elevamos la excepción `IllegalArgumentException` cuando se pasa un número de botellas pequeñas negativo de entrada, mientras que ellos devuelven `-1`. Lo que hemos hecho para adecuar el test y que pase correctamente es, en vez de decirle que espera la excepción `IllegalArgumentException`, poner un `assertTrue` comprobando que se devuelve `-1`.
		2. En `testForZeroBotellas` ocurre exactamente lo mismo que en el test anterior.
		3. En `testForZeroTotal`. En este caso ellos devuelven `0`, en vez de una excepción como nosotros. Así que para comprobar que el test pasa satisfactoriamente lo que hemos hecho es borrar la línea en la que indicamos que se esperaba la excepción `IllegalArgumentException` y hemos puesto un `assertTrue` para comprobar que devuelve un `0` el método calculaBotellasPequenas() cuando se le pasa una entrada con total 0.
		4. En `testForNegativeGrandes` ocurre exactamente lo mismo que en el test 1.
		5. En `testForNegativeTotal` ocurre exactamente lo mismo que en el test 1.
- **Apartado 4.** Enlace de GitHub a `EmbotelladoraTest2.java` adaptado a su SUT:
	- [Link al fichero de tests modificado](https://github.com/Onac8/nshandra_Practica-ISI/commit/b5dfb65f6508dde1309da2a0246ace21079eaaa6)

## Ejercicio 4 - Descuento BlackFriday
- **Apartado 1.** Enlace de GitHub al código que contiene el fallo:
	- [Link al SUT](https://github.com/Onac8/nshandra_Practica-ISI/blob/master/pruebasIDM/DescuentoBlackFriday/DescuentoBlackFriday.java)
	- [Link al fichero de tests](https://github.com/Onac8/nshandra_Practica-ISI/commit/f2b794bb94faefe442fdb5c960e951220ffb7512)
- **Apartados 2-3.**	Descripción de fallos y adaptaciones de nuestros tests para probar el código del otro grupo:
	- Hemos tenido, primeramente, que adecuar nuestros test al método `PrecioFinal()` de ellos, declarando las variables `int day` e `int month` antes de hacer cada test e inicializándolas a los valores correspondientes para que evaluasen el test de forma apropiada. Tras ello, 1 error obtenido tras pasar los 4 test:
		1. En `testForValidPrice`, debido a que tienen un fallo en su código ya que devuelven, en caso de ser BlackFriday, el descuento aplicado al producto, en lugar del precio del producto final tras ser rebajado.
- **Apartado 4.** Enlace de GitHub a `DescuentoBlackFridayTest2.java` adaptado a su SUT:
	- [Link al fichero de tests modificado](https://github.com/Onac8/nshandra_Practica-ISI/commit/929ad73861790dbaee406fe54d3e8f9093a56a5c)
