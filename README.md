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
# Enlaces
diferencia entre print y echo
https://www.it-swarm-es.com/es/php/cual-es-la-diferencia-entre-echo-print-y-print-r-en-php/968854098/

PHP CLI
https://replit.com/languages/PHP

EJEMPLOS PHP
https://www.w3schools.com/php/
