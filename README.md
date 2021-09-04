# IACC-INTPG1301
634-2021

EJEMPLO CON CLI
```php
<?php

function sumar() {
	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1+$n_2;
}

function restar() {
  	$n_1 = readline('INGRESE PRIMER NUMERO: ');
	$n_2 = readline('INGRESE SEGUNDO NUMERO: ');
    echo $n_1-$n_2;
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
    echo "OPCION INVALIDA";
}


?>
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
# Enlaces
PHP CLI
https://replit.com/languages/PHP

EJEMPLOS PHP
https://www.w3schools.com/php/
