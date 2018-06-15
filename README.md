# Simplex

Este fue un proyecto realizado para el curso de Investigacion de Operaciones de Instituo Tecnologico de Costa Rica.

Los creadores de este programa son:

Alonso Rivas S.
Edisson Lopez 

I. DESCRIPCION GENERAL
Se debe programar el algoritmo de SIMPLEX visto en clases para resolver problemas de Programacion Lineal (LP). La salida sera una presentacion Beamer que incluya el problema original, su solucion final y, si el usuario lo solicita, todas las tablas intermedias. Habra una interfaz gr ´ afica preparada con GTK y Glade para el ingreso de los problemas. Toda la
programacion debe realizarse en C sobre Linux. No se pueden cambiar las especificaciones de este documento.

II. ENTRADA
Usando una interfaz grafica apropiada, el usuario ingresara el modelo del problema que deba ser resuelto. Esto incluye:

Nombre del problema.

Nombres de las variables. Dado que la salida finales codigo LATEX estos nombres se pueden interpretar como hileras LATEX que seran insertadas en el documento final. Por defecto, estos nombres seran´ x1, x2, etc. - notese el uso de sub ındices.

Funcion objetivo. Verbo y ecuacion. 

Restricciones. Se manejara un maximo de 8 variables ´
y 10 restricciones (las restricciones triviales no se ingresan). Las restricciones pueden ser de la forma “≤”, “≥” o “=”.

III. SALIDA
Cuando el usuario considere que su problema ya esta listo, presionara algun boton para arrancar la ejecucion del algoritmo. Tambien indicara si desea las tablas intermedias. Se debe generar un archivo “.tex” que sera compilado con pdflatex o algun equivalente para que se produzca un archivo “pdf” que debe ser desplegado usando evince (o algun equivalente) en modo presentacion. La invocacion de todos estos comandos debe realizarse internamente desde su programa, de manera transparente para el usuario. Deben quedar disponibles tanto el pdf como el fuente de LATEX. Recuerde que su salida final sera una excelente presentacion Beamer.
En su presentacion deben aparecer los siguientes elementos:

1. Portada: se identifica claramente a los miembros del grupo, el curso, el semestre y el nombre del proyecto.

2. Algoritmo Sımplex: uno o dos slides que expliquen un poco el algoritmo Sımplex.

3. Problema original: presentar de manera matematica el problema original. Se deben respetar los nombres de variables escogidos por el usuario. 

4. Tabla Inicial: se muestra la Tabla Sımplex inicial. Esta podr´ıa incluir variables de holgura, variables de exceso, y variables artificiales. Se deben respetar los nombres de variables escogidos por el usuario.

5. Tablas Intermedias: si el usuario lo solicita, se deben presentar las tablas intermedias de la ejecucion del algoritmo. Debe aparecer marcada la columna seleccionada, los calculos de fracciones y el pivote. Si una variable artificial sale de la base, esta columna debe ser omitida en todas las tablas siguientes. Se deben respetar los nombres de variables escogidos por el usuario.

6. Tabla Final: se muestra la ultima Tabla Sımplex encontrada. Esta podr´ıa incluir variables de holgura,
variables de exceso, y variables artificiales. Se deben respetar los nombres de variables escogidos por el
usuario.
7. Solucion: se da la solucion optima encontrada con todo detalle. Si hubiera algun caso particular (e.g., problema no acotado, problema no factible, problema degenerado, etc.) la presentacion´ Beamer debe explicar porque el problema particular tiene esa condicion. Si hubiera soluciones multiples, el programa encontrara al menos 4 soluciones optimas diferentes, y las presentara junto con la ecuacion correspondiente. 


IV. Compilacion

Se debe ejecutar el comando: 

gcc -o gladewin main.c -Wall `pkg-config --cflags --libs gtk+-3.0` -export-dynamic -w


V. Ambiente
Fue disenado para Ubuntu.


