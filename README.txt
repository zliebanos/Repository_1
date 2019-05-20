kuboFinancieroApp

Requisiciones: tener instalada java 1.8 o superior.

1. Descargar el arhivo Examen Práctico TI SR.rar y descomprimir el archivo.

2. Abrir una línea de comandos en modo administrador.

3. Navegar hasta el directorio donde se descargó el fichero en la línea de comandos y ejecutar el siguiente comando: java -jar kuboFinancieroApp.jar

4. El programa cuenta con las siguientes operaciones (a continuación se listan los comandos para realizar las operaciones y se describe dicha operación):

   Comando		Ejemplo de uso:											Descripción
	- add 		./application add {“name”: “Juan Antonio Perez”}		(Agrega un nombre de persona en formato json en el archivo fuzzy-search.txt)
				
	- list  	./application list										(* Regresa todos los usuarios en orden alfabético en formato json, que se encuentran en el archivo. Si
																		 no hubiera usuarios agregados regresará una lista vacía en el siguiente formato:
																		 ./application list
																		 []
			
																		 * Si tuviera usuarios regresará en el siguiente formato:
																		 ./application list
																			[
																			{“name”: “Alberto Vera Padrón”},
																			{“name”: “Juan Antonio Perez”},
																			{“name”: “Rodolfo Juarez Fernandez”}
																			]
																	    )
																		
	- search 	./application fuzzy-search {“search”: “Alver”}			(* Busca dentro de los nombres del archivo y hace un fuzzy search, regresando el
																		   usuario con más aproximaciones.
				{“name”: “Alberto Vera Padrón”}							 * Si no hubiera coincidencias regresaría:
																		 
																		  ./application fuzzy-search {“search”: “Alver”}
																			Sin coincidencias
																		)
																		
5. Al presionar la tecla "Enter" se ejecutará el comando ingresado por teclado.

6. A continuación se explica la definición del algoritmo de búsqueda de aproximación y la razón para elegirlo:
	Consiste en recorrer y examinar cada uno de los elementos del array hasta encontrar el o los elementos buscados, o hasta que se han mirado todos los elementos del array.
	Ya que nuestra información se puede encontrar completamente desordenada, es el único algoritmo que nos puede ayudar a encontrar el dato que buscamos.