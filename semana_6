```
Algoritmo algoritmo_semana_6_jhonnattan_rivera
	// no se permiten , ni letras mayusculas, ni acentuadas ni . ni cualiquier parametro
	// que no sea una vocal o una consonante
	
	//paso0 : definir el tipo de dato
	Definir palabra, palabra_invertida Como Caracter

	//paso1 : definir mi palabra.
	palabra = "No subas, abusón"
	cantidad_caracteres = Longitud(palabra)
	
	//paso2 : definir mi palabra pero invertida.
	Para i=0 Hasta cantidad_caracteres con Paso 1 Hacer
		
		// palabra_invertida = palabra_invertida + SubCadena(palabra,0,1)
		letra_iteracion = SubCadena(palabra,cantidad_caracteres-i,cantidad_caracteres-i)
		palabra_invertida = palabra_invertida + letra_iteracion;
		
	FinPara
	
	Escribir palabra
	Escribir palabra_invertida
	resultado = "es palindromo"
	
	palabra_sin_espacios = ""
	palabra_invertida_sin_espacios = ""

	//eliminar espacios
	Para i=1 Hasta cantidad_caracteres con Paso 1 Hacer
		letra_iteracion_palabra = SubCadena(palabra,i,i)
		letra_iteracion_palabra_invertida = SubCadena(palabra_invertida,i,i)
		
		si letra_iteracion_palabra <> " " Entonces
			palabra_sin_espacios = palabra_sin_espacios + letra_iteracion_palabra
		FinSi
		
		si letra_iteracion_palabra_invertida <> " " Entonces
			palabra_invertida_sin_espacios = palabra_invertida_sin_espacios + letra_iteracion_palabra_invertida
		FinSi
		
	FinPara
	
	//paso2 : comparar cada letra de la palabra y la palabra invertida.
	cantidad_caracteres_sin_espacios = Longitud(palabra_sin_espacios)
	Para i=1 Hasta cantidad_caracteres_sin_espacios con Paso 1 Hacer
		letra_iteracion_palabra = SubCadena(palabra_sin_espacios,i,i)
		letra_iteracion_palabra_invertida = SubCadena(palabra_invertida_sin_espacios,i,i)

		si letra_iteracion_palabra <> letra_iteracion_palabra_invertida Entonces
			Escribir "letras distintas"
			resultado = "no es palindromo"
		SiNo 
			Escribir "letras iguales"
		finsi
		
	FinPara
	
	Escribir resultado;
	
FinAlgoritmo
```
