                           PARA COMPILAR


  Para compilar nuestro programa primero ejecutamos en la consola la
siguiente linea:

----------------------------------------------------------------
$ gcc -std=c99 -Wall -c tablahash.c btree.c corrector.c hlist.c
----------------------------------------------------------------

  Luego, si todo salió bien, generó cuatro archivo .o en el directorio.

  Ejecutamos la siguiente orden: 

---------------------------------------------------------------------------
$ gcc -std=c99 -Wall -o main main.c tablahash.o btree.o corrector.o hlist.o
---------------------------------------------------------------------------

  Creandonos main en la misma carpeta.

  Ejecutamos la siguiente linea donde "archivoEntrada" es el texto al que queremos
aplicarle las sugerencias y "archivoSalida" es archivo donde nos va a imprimir
todas las palabras que no están en nuestro Universo y sus respectivas sugerencias.
  Estos archivos deben estar en la misma carpeta donde se vaya a ejecutar el programa.
  En el archivo de entrada al final tiene que haber un enter (\n) para que el
lector del archivo funcione siempre bien. 

-------------------------------------
$ ./main archivoEntrada archivoSalida
-------------------------------------


                              SOBRE NUESTRO CÓDIGO
 
En la primera parte del código usamos una tabla hash para representar nuestro universo
de palabras, ya que la búsqueda es rápida en comparación a otros tipos de estructuras 
dados en la materia. Las colisiones se resuelven por encadenamiento con estructura AVL.
En la segunda parte las sugerencias se resuelven con árboles y las listas posibles se 
resuelve con listas enlazadas ya que solo hay que agregar al final y tomar el primero nodo.



