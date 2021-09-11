```
## ejemplo creado en la junta con pseudocodigo

Algoritmo algoritmo_semana_6_jhonnattan_rivera
	// no se permiten , ni letras mayusculas, ni acentuadas ni . ni cualiquier parametro
	// que no sea una vocal o una consonante
	
	//paso0 : definir el tipo de dato
	Definir palabra, palabra_invertida Como Caracter

	//paso1 : definir mi palabra.
	palabra = "luz azul"
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


## ejemplo en PHP
```php
<?php
/**
 * Funcion para determinar si un texto es polindromo
 *
 * @param string $cadena
 * @return boolean
 */
function esPolindromo($cadena)
{
    if (strlen($cadena)<2) {
        return false;
    }
 
    # eliminamos los espacios, comas, puntos y convertimos la cadena en minusculas
    $cadena=strtolower(str_replace([" ", ",", "."], "", $cadena));
 
    for ($i=0;$i<strlen($cadena);$i++) {
        if ($cadena[$i]!=$cadena[strlen($cadena)-$i-1]) {
            return false;
        }
    }
    return true;
}
 
 
echo esPolindromo("casa");                      // false
echo esPolindromo("Isaac no ronca asi");        // true
echo esPolindromo("Yo dono rosas, oro no doy"); // true
echo esPolindromo("12521");                     // true
```

## Fuentes:
https://www.lawebdelprogramador.com/codigo/PHP/5408-Funcion-para-determinar-si-una-cadena-es-palindromo.html