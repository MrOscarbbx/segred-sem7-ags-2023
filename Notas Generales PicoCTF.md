
Para Decodificar Archivos según su formato :

	iconv -f <Formato en el que esta > -t <Formato al que se pasa > enc 

Para convertir de Decimal a Ascii :

	texto | awk '{ printf "%c", $1 }';

Para convertir de Hexa a Decimal

	printf "%d\n" 0X3D 

Para poder convertir casi todo solo cambiar las bases

	echo "ibase=10;obase=2;42" | bc

En C se puede usando "%x" leer los datos de un stack que se haya utilizado para almacenar informacion.

xxd sirve para decodificar Hexadecimal

	xxd -r -p