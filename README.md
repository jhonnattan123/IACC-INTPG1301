# IACC-INTPG1301
634-2021

## Ejemplos:

### con PHP CLI
```php
<?php
function sumar() {
	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1+$n_2."\n"; // \n es un salto de linea osea un enter
}
function restar() {
  	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1-$n_2."\n";
}
$opcion = readline('SELECCIONE UNA OPCION (SUMAR|RESTAR): ');
switch ($opcion) {
  case "SUMAR":
    sumar();
  break;
  case "RESTAR":
    restar();
    break;
  default:
    echo "OPCION INVALIDA\n";
}
?>
```

### Pseudocodigo:

```pSeInt
Funcion SUMAR (  )
	Definir n1,n2 Como real
	Escribir 'INGRESE PRIMER NUMERO: '
	leer n1
	Escribir 'INGRESE SEGUNDO NUMERO: '
	leer n2
	Escribir n1+n2
Fin Funcion

Funcion RESTAR (  )
	Definir n1,n2 Como real
	Escribir 'INGRESE PRIMER NUMERO: '
	leer n1
	Escribir 'INGRESE SEGUNDO NUMERO: '
	leer n2
	Escribir n1-n2
Fin Funcion

Algoritmo ejemplo_php_1
	
	Definir opcion Como Caracter
	Escribir('SELECCIONE UNA OPCION (SUMAR|RESTAR): ')
	leer opcion
	
	Segun opcion hacer
		'SUMAR':
			SUMAR()
		'RESTAR':
			RESTAR()
		De otro modo:
			Escribir "OPCION INVALIDA"
	FinSegun
	
			
FinAlgoritmo
```


EJEMPLO CLI CON 3 REPETICIONES
```php
<?php

function sumar() {
	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1+$n_2."\n";
}

function restar() {
  	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1-$n_2."\n";
}


for ($x = 1; $x <= 3; $x++) {
  $opcion = readline('SELECCIONE UNA OPCION (SUMAR|RESTAR): ');
	switch ($opcion) {
	  case "SUMAR":
	    sumar();
	  break;
	  case "RESTAR":
	    restar();
	    break;
	  default:
	    echo "OPCION INVALIDA\n";
	}
}


exit();

?>
```


ejemplo sin CLI
```php
<?php

$n_1 = 60;
$n_2 = 10.5;
$opcion = "RESTAR";

switch($opcion){
	case "SUMAR":
    	echo "tu resultado es :";
        echo $n_1 + $n_2;
    break;
    
    case "RESTAR":
    	echo "tu resultado es :";
    	echo $n_1 - $n_2;
    break;
    
    default:
    	echo "NO EXISTE OPCION";

};

?>
```



ejemplo bucle CLI
```php
<?php
function sumar() {
	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1+$n_2."\n";
}

function restar() {
  	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1-$n_2."\n";
}
$continuar = "si";
while($continuar == "si") {
	$opcion = readline('SELECCIONE UNA OPCION (SUMAR|RESTAR): ');
	switch ($opcion) {
		case "SUMAR":
			sumar();
		break;
		case "RESTAR":
			restar();
		break;
		default:
			echo "OPCION INVALIDA\n";
	}
	$continuar = readline('QUIERE CONTINUAR (si/no)');
}

?>
```


ejemplo pseudocodigo para exponente
```
SubProceso  resultado <- Potencia (base, exponente)
    Si exponente=0 Entonces
        resultado <- 1;
    sino 
        resultado <- base*Potencia(base,exponente-1); 
    FinSi
FinSubProceso

Proceso DosALaDiezRecursivo
    Escribir "Ingrese Base"
    Leer base
    Escribir "Ingrese Exponente"
    Leer exponente
    Escribir "El resultado es ",Potencia(base,exponente)
FinProceso

```


### EJEMPLO CON FORMULARIO HTML Y UN ARCHIVO PHP
el archivo con el formulario se debe llamar index.php

```html
<form action="/calcular.php">
    <label for="primer_numero">Primer numero:</label><br>
    <input type="number" id="primer_numero" name="primer_numero">
	<br>
  	<label for="segundo_numero">Segundo numero:</label><br>
  	<input type="number" id="segundo_numero" name="segundo_numero">
    	<br>
        <label for="operacion">Seleccione operacion:</label><br>
	<select id="operacion" name="operacion">
		<option value="SUMAR"> SUMAR </option>
  		<option value="RESTAR"> RESTAR </option>
        </select>
	<br>
	<br>
  	<input type="submit" value="Enviar">
</form> 

</body>
</html>

```

el archivo con el algoritmo se debe llamar calculo.php
```php
<?php
$primer_numero = $_GET["primer_numero"];
$segundo_numero = $_GET["segundo_numero"];
$operacion = $_GET["operacion"];

function SUMAR( $n1, $n2 ){
	return $n1 + $n2;
}

function RESTAR( $n1, $n2 ){
	return $n1 - $n2;
}

switch($operacion){
	case"SUMAR":
		$resultado = SUMAR( $primer_numero, $segundo_numero );
	break;
	case"RESTAR":
		$resultado = RESTAR( $primer_numero, $segundo_numero );
	break;
	default:
}

print("resultado : ".$resultado."<br>");
?>

<a href="./">volver</a>
```


# Enlaces
diferencia entre print y echo
https://www.it-swarm-es.com/es/php/cual-es-la-diferencia-entre-echo-print-y-print-r-en-php/968854098/

PHP CLI
https://replit.com/languages/PHP

EJEMPLOS PHP
https://www.w3schools.com/php/

XAMMP para correr PHP en nuestra computadora
https://www.apachefriends.org/es/index.html
