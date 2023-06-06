SubProceso modificar <- modificar ( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1)
	Definir Nom_pro Como Caracter;
	Definir cont Como Entero;
	cont<-0;
	Segun opc Hacer
		1:
			Segun opc_1 Hacer
				1:
					//Le pedimos al usuario el nombre del producto a buscar
					Escribir "Cual es el nombre del producto a cambiar el precio ?";
					Leer Nom_pro;
					Para i<-1 Hasta imp Con Paso 1 Hacer
						Para j<-1 Hasta 2 Con Paso 1 Hacer
							Si j==1 Entonces
								//comparamos el nombre que el cliente ingreso anteriormente con el de la pocision de la matriz
								Si Nom_pro==tintacontinua[i,j] Entonces
									Escribir "modificar el articulo ",tintacontinua[i,j];
									//Determinamos que el nombre es el mismo
									cont<-1;
								SiNo
									cont<-2;
									
								FinSi
							SiNo
								Si cont==1 Entonces
									//Ingresamos el nuevo precio
									Leer tintacontinua[i,j];
								SiNo
									Limpiar Pantalla;
								FinSi
								
							FinSi
						FinPara
					FinPara
				2:
					//Le pedimos al usuario el nombre del producto a buscar
					Escribir "Cual es el nombre del producto a cambiar el precio ?";
					Leer Nom_pro;
					Para i<-1 Hasta pap Con Paso 1 Hacer
						Para j<-1 Hasta 2 Con Paso 1 Hacer
							Si j==1 Entonces
								//comparamos el nombre que el cliente ingreso anteriormente con el de la pocision de la matriz
								Si Nom_pro==laser[i,j] Entonces
									Escribir "modificar el articulo ",laser[i,j];
									//Determinamos que el nombre es el mismo
									cont<-1;
								SiNo
									cont<-2;
								FinSi
							SiNo
								Si cont==1 Entonces
									//Ingresamos el nuevo precio
									Leer laser[i,j];
								SiNo
									Limpiar Pantalla;
								FinSi
							FinSi
						FinPara
					FinPara
			FinSegun
		2:
			Segun opc_1 Hacer
				1:
					//Le pedimos al usuario el nombre del producto a buscar
					Escribir "Cual es el nombre del producto a cambiar el precio ?";
					Leer Nom_pro;
					Para i<-1 Hasta pro Con Paso 1 Hacer
						Para j<-1 Hasta 2 Con Paso 1 Hacer
							Si j==1 Entonces
								//comparamos el nombre que el cliente ingreso anteriormente con el de la pocision de la matriz
								Si Nom_pro==tinta[i,j]  Entonces
									Escribir "modificar el articulo ",tinta[i,j];
									//Determinamos que el nombre es el mismo
									cont<-1;
								SiNo
									cont<-2;
								FinSi
							SiNo
								Si cont==1 Entonces
									//Ingresamos el nuevo precio
									Leer tinta[i,j];
								SiNo
									Limpiar Pantalla;
								FinSi
							FinSi
						FinPara
					FinPara
				2:
					//Le pedimos al usuario el nombre del producto a buscar
					Escribir "Cual es el nombre del producto a cambiar el precio ?";
					Leer Nom_pro;
					Para i<-1 Hasta sem Con Paso 1 Hacer
						Para j<-1 Hasta 2 Con Paso 1 Hacer
							Si j==1 Entonces
								//comparamos el nombre que el cliente ingreso anteriormente con el de la pocision de la matriz
								Si Nom_pro==repuestos[i,j] Entonces
									Escribir "modificar el articulo ",repuestos[i,j];
									//Determinamos que el nombre es el mismo
									cont<-1;
								SiNo
									cont<-2;
									
								FinSi
							SiNo
								Si cont==1 Entonces
									//Ingresamos el nuevo precio
									Leer repuestos[i,j];
								SiNo
									Limpiar Pantalla;
								FinSi
								
							FinSi
						FinPara
					FinPara
			FinSegun
		3:
			Segun opc_1 Hacer
				1:
					//Le pedimos al usuario el nombre del producto a buscar
					Escribir "Cual es el nombre del producto a cambiar el precio ?";
					Leer Nom_pro;
					Para i<-1 Hasta pil Con Paso 1 Hacer
						Para j<-1 Hasta 2 Con Paso 1 Hacer
							Si j==1 Entonces
								//comparamos el nombre que el cliente ingreso anteriormente con el de la pocision de la matriz
								Si Nom_pro==sellos[i,j] Entonces
									Escribir "modificar el articulo ",sellos[i,j];
									//Determinamos que el nombre es el mismo
									cont<-1;
								SiNo
									cont<-2;
									
								FinSi
							SiNo
								Si cont==1 Entonces
									//Ingresamos el nuevo precio
									Leer sellos[i,j];
								SiNo
									Limpiar Pantalla;
								FinSi
								
							FinSi
						FinPara
					FinPara
			FinSegun
	FinSegun
FinSubProceso

//subcatalogo
SubProceso sub_catalogo <- subcat ( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1 )
	Definir seguir Como Caracter;
	//Determinamos la opcion del catalogo principal
	Segun opc Hacer
		1:
			//Determinamos que subcatalogo queremos imprimir 
			Segun opc_1 Hacer
				1:
					//Determinamos si la matriz esta vacia
					Si imp>0 Entonces
						//Si la matriz cuenta con articulos, imprimimos los mismos
						Para i<-1 Hasta imp Con Paso 1 Hacer
							Escribir Sin Saltar"Articulo: ",i," ";
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir Sin Saltar tintacontinua[i,j]," || ";
								SiNo
									Escribir Sin Saltar tintacontinua[i,j]," || ";
								FinSi
							FinPara
							Escribir "";
						FinPara
						Leer seguir;
					//Si la matriz esta vacia se imprime el mensaje
					SiNo
						Escribir "Esta seccion esta vacia";
					FinSi
				2:
					//Determinamos si la matriz esta vacia
					Si pap>0 Entonces
						//Si la matriz cuenta con articulos, imprimimos los mismos
						Para i<-1 Hasta pap Con Paso 1 Hacer
							Escribir Sin Saltar"Articulo: ",i," ";
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir Sin Saltar laser[i,j]," || ";
								SiNo
									Escribir Sin Saltar laser[i,j]," || ";
								FinSi
							FinPara
							Escribir "";
						FinPara
						Leer seguir;
					//Si la matriz esta vacia se imprime el mensaje
					SiNo
						Escribir "Esta seccion esta vacia";
					FinSi
			FinSegun
		2:
			Segun opc_1 Hacer
				1:
					//Determinamos si la matriz esta vacia
					Si pro>0 Entonces
						//Si la matriz cuenta con articulos, imprimimos los mismos
						Para i<-1 Hasta pro Con Paso 1 Hacer
							Escribir Sin Saltar"Articulo: ",i," ";
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir Sin Saltar tinta[i,j]," || ";
								SiNo
									Escribir Sin Saltar tinta[i,j]," || ";
								FinSi
							FinPara
							Escribir "";
						FinPara
						Leer seguir;
					//Si la matriz esta vacia se imprime el mensaje	
					SiNo
						Escribir "Esta seccion esta vacia";
					FinSi
				2:
					//Determinamos si la matriz esta vacia
					Si sem>0 Entonces
						//Si la matriz cuenta con articulos, imprimimos los mismos
						Para i<-1 Hasta sem Con Paso 1 Hacer
							Escribir Sin Saltar"Articulo: ",i," ";
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir Sin Saltar repuestos[i,j]," || ";
								SiNo
									Escribir Sin Saltar repuestos[i,j]," || ";
								FinSi
							FinPara
							Escribir "";
						FinPara
						Leer seguir;
					//Si la matriz esta vacia se imprime el mensaje	
					SiNo
						Escribir "Esta seccion esta vacia";
					FinSi
			FinSegun
		3:
			Segun opc_1 Hacer
				1:
					//Determinamos si la matriz esta vacia
					Si pil>0 Entonces
						//Si la matriz cuenta con articulos, imprimimos los mismos
						Para i<-1 Hasta pil Con Paso 1 Hacer
							Escribir Sin Saltar"Articulo: ",i," ";
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir Sin Saltar sellos[i,j]," || ";
								SiNo
									Escribir Sin Saltar sellos[i,j]," || ";
								FinSi
							FinPara
							Escribir "";
						FinPara
						Leer seguir;
					//Si la matriz esta vacia se imprime el mensaje	
					SiNo
						Escribir "Esta seccion esta vacia";
					FinSi
			FinSegun
	FinSegun
FinSubProceso

//Modificamos precios
SubProceso modif <- modif ( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny )
	Definir opc,opc_1 Como Entero;
	Repetir
		//Mostramos el catalogo principal
		Escribir "Modificar: ";
		Escribir "";
		Escribir "1. Impresoras";
		Escribir "2. Suministros";
		Escribir "3. Sellos";
		Escribir "4. volver";
		Leer opc;
		Segun opc Hacer
			1:
				//Mostramos el Subcatalogo de Impresoras
				Limpiar Pantalla;
				Escribir "Seccion Impresoras";
				Escribir "";
				Escribir "1. Tinta continua";
				Escribir "2. laser";
				//Le pedimos al usuario la opcion a modificar
				Leer opc_1;
				//Llamamos a la Funcion "modifucar" que se encarga de modificar un precia de un producto
				Escribir modificar(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
			2:
				//Mostramos el subcatalogo de Suministros
				Limpiar Pantalla;
				Escribir "Seccion Suministros";
				Escribir "";
				Escribir "1. Tintas";
				Escribir "2. Repuestos";
				//Le pedimos al usuario la opcion a modificar
				Leer opc_1;
				//Llamamos a la Funcion "modifucar" que se encarga de modificar un precia de un producto
				Escribir modificar(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
			3:
				//Mostramos el subcatalogo de Sellos
				Limpiar Pantalla;
				Escribir "Seccion Sellos";
				Escribir "";
				Escribir "1. Sellos";
				//Le pedimos al usuario la opcion a modificar
				Leer opc_1;
				//Llamamos a la Funcion "modifucar" que se encarga de modificar un precia de un producto
				Escribir modificar(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
		FinSegun
	Hasta Que opc==4
	
FinSubProceso

//Añadimos nuevos productos producto
SubProceso añadir <- add_n (tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1)
	Segun opc Hacer
		1:
			Segun opc_1 Hacer
				1:
					//Validamos si es la primera fila o primer producto
					Si imp==1 Entonces
						//Si es el caso, se ingresa en la fila 1
						Para i<-1 Hasta imp Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer tintacontinua[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer tintacontinua[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
					//Si la matriz ya cuenta productos, se agrega el producto en la pocision imp
					Si imp>1 Entonces
						Para i<-imp Hasta imp Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer tintacontinua[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer tintacontinua[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
				2:
					//Validamos si es la primera fila o primer producto
					Si pap==1 Entonces
						//Si es el caso, se ingresa en la fila 1
						Para i<-1 Hasta pap Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer laser[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer laser[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
					//Si la matriz ya cuenta productos, se agrega el producto en la pocision pap
					Si pap>1 Entonces
						Para i<-pap Hasta pap Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer laser[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer laser[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
				
			FinSegun
		2:
			Segun opc_1 Hacer
				1:
					//Validamos si es la primera fila o primer producto
					Si pro==1 Entonces
						//Si es el caso, se ingresa en la fila 1
						Para i<-1 Hasta pro Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer tinta[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer tinta[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
					//Si la matriz ya cuenta productos, se agrega el producto en la pocision pro
					Si pro>1 Entonces
						Para i<-pro Hasta pro Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer tinta[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer tinta[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
				2:
					//Validamos si es la primera fila o primer producto
					Si sem==1 Entonces
						//Si es el caso, se ingresa en la fila 1
						Para i<-1 Hasta sem Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer repuestos[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer repuestos[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
					//Si la matriz ya cuenta productos, se agrega el producto en la pocision sem
					Si sem>1 Entonces
						Para i<-sem Hasta sem Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer repuestos[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer repuestos[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
			FinSegun
		3:
			Segun opc_1 Hacer
				1:
					//Validamos si es la primera fila o primer producto
					Si pil==1 Entonces
						//Si es el caso, se ingresa en la fila 1
						Para i<-1 Hasta pil Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer sellos[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer sellos[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
					//Si la matriz ya cuenta productos, se agrega el producto en la pocision pil
					Si pil>1 Entonces
						Para i<-pil Hasta pil Con Paso 1 Hacer
							Para j<-1 Hasta 2 Con Paso 1 Hacer
								Si j==1 Entonces
									Escribir "Ingrese el nombre del articulo ",i;
									Leer sellos[i,j];
								SiNo
									Escribir "Ingrese el precio del articulo ",i;
									Leer sellos[i,j];
								FinSi
							FinPara
						FinPara
					FinSi
			FinSegun
	FinSegun
FinSubProceso

//catalogo
SubProceso ver_catalogo <- vcat ( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny)
	Definir opc,opc_1 Como Entero;
	Repetir
		//Mostramos el catalogo principal
		Limpiar Pantalla;
		Escribir "Catalogo";
		Escribir "";
		Escribir "1. Impresoras";
		Escribir "2. Suministros";
		Escribir "3. Sellos";
		Escribir "4. volver";
		Leer opc;
		opc_1<-0;
		//Ingresamos al catalogo que eligió el usuario
		Segun opc Hacer
			1:
				//Subcatlogo del catalogo Impresoras
				Limpiar Pantalla;
				Escribir "Seccion Impresoras";
				Escribir "";
				Escribir "1. Tinta continua";
				Escribir "2. laser";
				Leer opc_1;
				//Llamamos a la Funcion "subcat" que se encarga de mostrar el subcatalogo elegido por el usuario
				Escribir subcat( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1 );
			2:
				//Subcatalogo del catalogo Suministros
				Limpiar Pantalla;
				Escribir "Seccion Suministros";
				Escribir "";
				Escribir "1. Tintas";
				Escribir "2. Repuestos";
				Leer opc_1;
				//Llamamos a la Funcion "subcat" que se encarga de mostrar el subcatalogo elegido por el usuario
				Escribir subcat( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1 );
			3:
				//Subcatalogo del catalogo Sellos
				Limpiar Pantalla;
				Escribir "Seccion Sellos";
				Escribir "";
				Escribir "1. Sellos";
				Leer opc_1;
				//Llamamos a la Funcion "subcat" que se encarga de mostrar el subcatalogo elegido por el usuario
				Escribir subcat( tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1 );
		FinSegun
	Hasta Que opc==4
	
FinSubProceso

//menu
SubProceso menu <- menu (tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny)
	Definir men,salir Como Entero;
	Definir opc,opc_1 Como Entero;
	Repetir
		//Mostramos las funcionalidades principales
		Limpiar Pantalla;
		Escribir "menú";
		Escribir "";
		Escribir "1. Ver catalogo";
		Escribir "2. Añadir productos";
		Escribir "3. Modificar precio de producto";
		Escribir "4. Salir";
		Leer men;
		//ejecutamos la funcion elegida por el usuario
		Segun men Hacer
			//opcion 1
			1:
				//Llamamos a la funcion "vcat" la cual se encarga de mostrar los subcatalogos de cada catalogo
				Escribir vcat(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny);
			2:
				Repetir
					//Mostramos el catalogo principal
					Limpiar Pantalla;
					Escribir "Añadir producto a:";
					Escribir "";
					Escribir "1. Impresoras";
					Escribir "2. Suministros";
					Escribir "3. Sellos";
					Escribir "4. volver";
					Leer opc;
					opc_1<-0;
					Segun opc Hacer
						1:
							//Mostramos el subcatalogo de Impresoras
							Limpiar Pantalla;
							Escribir "Seccion Impresoras";
							Escribir "";
							Escribir "1. Tinta continua";
							Escribir "2. laser";
							Leer opc_1;
							//Determinamos a que seccion se va agregar un producto
							Segun opc_1 Hacer
								1:
									//Se suma 1 al contador para añadir una nueva fila en la matriz
									imp<-imp+1;
									//Llamamos a la Funcion "add_n" que se encarga de agregar un nuevo articulo 
									Escribir add_n(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
								2:
									//Se suma 1 al contador para añadir una nueva fila en la matriz
									pap<-pap+1;
									//Llamamos a la Funcion "add_n" que se encarga de agregar un nuevo articulo 
									Escribir add_n(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
							FinSegun
							
						2:
							//Mostramos el subcatalogo de Impresoras
							Limpiar Pantalla;
							Escribir "Seccion Suministros";
							Escribir "";
							Escribir "1. Tintas";
							Escribir "2. Repuestos";
							Leer opc_1;
							//Determinamos a que seccion se va agregar un producto
							Segun opc_1 Hacer
								1:
									//Se suma 1 al contador para añadir una nueva fila en la matriz
									pro<-pro+1;
									//Llamamos a la Funcion "add_n" que se encarga de agregar un nuevo articulo 
									Escribir add_n(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
								2:
									//Se suma 1 al contador para añadir una nueva fila en la matriz
									sem<-sem+1;
									//Llamamos a la Funcion "add_n" que se encarga de agregar un nuevo articulo 
									Escribir add_n(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
							FinSegun
							
						3:
							//Mostramos el subcatalogo de Impresoras
							Limpiar Pantalla;
							Escribir "Seccion Sellos";
							Escribir "";
							Escribir "1. Sellos";
							Leer opc_1;
							//Determinamos a que seccion se va agregar un producto
							Segun opc_1 Hacer
								1:
									//Se suma 1 al contador para añadir una nueva fila en la matriz
									pil<-pil+1;
									//Llamamos a la Funcion "add_n" que se encarga de agregar un nuevo articulo 
									Escribir add_n(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny,opc,opc_1);
							FinSegun
							
					FinSegun
					;
				Hasta Que opc==4
				
			3:
				//LLamamos a la funcion "modif" que se encarga de mostrar el catalogo principal y sus subcatalogos a modificar
				Escribir modif(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny);
		FinSegun
	Hasta Que men==4
FinSubProceso

//se añade los productos de 0
SubProceso agregarpro <- Add_pro (tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny)
	Definir opc,cat Como Entero;
	Definir seg Como Caracter;
	Repetir
		//mostramos las categorias
		Limpiar Pantalla;
		Escribir "Añadir producto al catalogo de Mundo Copias";
		Escribir "";
		Escribir "1. Impresoras";
		Escribir "2. Suministros";
		Escribir "3. Sellos";
		Escribir "4. Ir al menú principal";
		Leer cat;
		Segun cat Hacer
			1:
				//mostramos las subcategorias de la categoria Impresoras
				Limpiar Pantalla;
				Escribir "Seccion Impresoras";
				Escribir "";
				Escribir "1. Tinta continua";
				Escribir "2. laser";
				Leer opc;
				Segun opc Hacer
					1:
						//Verificamos si la matriz esta vacia
						Si imp=0 Entonces
							//Si esta vacia permitimos agregar productos
							Limpiar Pantalla;
							Escribir "Ingrese el numero de productos a ingresar en la seccion ";
							Leer imp;
							Para i<-1 Hasta imp Con Paso 1 Hacer
								Limpiar Pantalla;
								Escribir "Articulo ",i;
								Escribir "";
								Para j<-1 Hasta 2 Con Paso 1 Hacer
									Si j==1 Entonces
										Escribir "Ingrese el nombre";
										Leer tintacontinua[i,j];
									SiNo
										Escribir "Ingrese el precio ";
										Leer tintacontinua[i,j];
									FinSi
								FinPara
							FinPara
						SiNo
							//Si la matriz ya cuenta con informacion, imprimimos este mensaje
							Escribir "Usted ya ingreso productos en esta seccion";
							Leer seg;
						FinSi
						
					2:
						//Verificamos si la matriz esta vacia
						Si pap==0 Entonces
							//Si esta vacia permitimos agregar productos
							Limpiar Pantalla;
							Escribir "Ingrese el numero de productos a ingresar en la seccion ";
							Leer pap;
							Para i<-1 Hasta pap Con Paso 1 Hacer
								Limpiar Pantalla;
								Escribir "Articulo ",i;
								Escribir "";
								Para j<-1 Hasta 2 Con Paso 1 Hacer
									Si j==1 Entonces
										Escribir "Ingrese el nombre";
										Leer laser[i,j];
									SiNo
										Escribir "Ingrese el precio";
										Leer laser[i,j];
									FinSi
								FinPara
							FinPara
						SiNo
							//Si la matriz ya cuenta con informacion, imprimimos este mensaje
							Escribir "Usted ya ingreso productos en esta seccion";
							Leer seg;
						FinSi
					De Otro Modo:
						Escribir "Opcion no valida";
				FinSegun
				
			2:
				//mostramos las subcategorias de la categoria Suministros
				Limpiar Pantalla;
				Escribir "Seccion Suministros";
				Escribir "";
				Escribir "1. Tinta";
				Escribir "2. Repuestos";
				Leer opc;
				Segun opc Hacer
					1:
						//Verificamos si la matriz esta vacia
						Si pro==0 Entonces
							//Si esta vacia permitimos agregar productos
							Limpiar Pantalla;
							Escribir "Ingrese el numero de productos a ingresar en la seccion ";
							Leer pro;
							Para i<-1 Hasta pro Con Paso 1 Hacer
								Limpiar Pantalla;
								Escribir "Articulo ",i;
								Escribir "";
								Para j<-1 Hasta 2 Con Paso 1 Hacer
									Si j==1 Entonces
										Escribir "Ingrese el nombre";
										Leer tinta[i,j];
									SiNo
										Escribir "Ingrese el precio ";
										Leer tinta[i,j];
									FinSi
								FinPara
							FinPara
						SiNo
							//Si la matriz ya cuenta con informacion, imprimimos este mensaje
							Escribir "Usted ya ingreso productos en esta seccion";
							Leer seg;
						FinSi
						
					2:
						//Verificamos si la matriz esta vacia
						Si sem==0 Entonces
							//Si esta vacia permitimos agregar productos
							Limpiar Pantalla;
							Escribir "Ingrese el numero de productos a ingresar en la seccion ";
							Leer sem;
							Para i<-1 Hasta sem Con Paso 1 Hacer
								Limpiar Pantalla;
								Escribir "Articulo ",i;
								Escribir "";
								Para j<-1 Hasta 2 Con Paso 1 Hacer
									Si j==1 Entonces
										Escribir "Ingrese el nombre";
										Leer repuestos[i,j];
									SiNo
										Escribir "Ingrese el precio ";
										Leer repuestos[i,j];
									FinSi
								FinPara
							FinPara
						SiNo
							//Si la matriz ya cuenta con informacion, imprimimos este mensaje
							Escribir "Usted ya ingreso productos en esta seccion";
							Leer seg;
						FinSi
					De Otro Modo:
						Escribir "opcion no valida";
				FinSegun
			3:
				//mostramos las subcategorias de la categoria Sellos
				Limpiar Pantalla;
				Escribir "Seccion Sellos";
				Escribir "";
				Escribir "1. Sellos";
				Leer opc;
				Segun opc Hacer
					1:
						//Verificamos si la matriz esta vacia
						Si pil==0 Entonces
							//Si esta vacia permitimos agregar productos
							Limpiar Pantalla;
							Escribir "Ingrese el numero de productos a ingresar en la seccion ";
							Leer pil;
							Para i<-1 Hasta pil Con Paso 1 Hacer
								Limpiar Pantalla;
								Escribir "Articulo ",i;
								Escribir "";
								Para j<-1 Hasta 2 Con Paso 1 Hacer
									Si j==1 Entonces
										Escribir "Ingrese el nombre";
										Leer sellos[i,j];
									SiNo
										Escribir "Ingrese el precio ";
										Leer sellos[i,j];
									FinSi
								FinPara
							FinPara
						SiNo
							//Si la matriz ya cuenta con informacion, imprimimos este mensaje
							Escribir "Usted ya ingreso productos en esta seccion";
							Leer seg;
						FinSi
						
					De Otro Modo:
						Escribir "opcion no valida";
				FinSegun
		FinSegun
	Hasta Que cat==4
	//Llamamos a la Funcion "menu", la cual se encarga de mostrarnos las opciones pricipales
	Escribir menu(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny);	
FinSubProceso

//programa principal
Proceso sin_titulo
	//Dimensionamos las matrices que vamos a utilizar
	Dimension tintacontinua[100,3];
	Dimension laser[100,3];
	Dimension tinta[100,3];
	Dimension repuestos[100,3];
	Dimension sellos[100,3];
	//Definimos las variables
	definir tintacontinua,laser,tinta,repuestos,sellos Como Caracter;
	Definir i,j,imp,pap,lap,pro,sem,veg,pil,iny Como Entero;
	//i sera la ubicacion X en todas las matrices
	i<-0;
	//j sera la ubicacion Y en todas las matrices
	j<-0;
	//imp sera el contador que determinará la cantidad de articulos que va tener la matriz "tintacontinua"
	imp<-0;
	//pap sera el contador que determinará la cantidad de articulos que va tener la matriz "laser"
	pap<-0;
	lap<-0;
	//pro sera el contador que determinará la cantidad de articulos que va tener la matriz "tinta"
	pro<-0;
	//sem sera el contador que determinará la cantidad de articulos que va tener la matriz "repuestos"
	sem<-0;
	veg<-0;
	//pil sera el contador que determinará la cantidad de articulos que va tener la matriz "sellos"
	pil<-0;
	iny<-0;
	//Llamamos a la Funcion "add_pro", la cual se encarga de agregar la cantidad de productos que querramos en cada matriz
	Escribir Add_pro(tintacontinua,laser,tinta,repuestos,sellos,i,j,imp,pap,lap,pro,sem,veg,pil,iny);
FinProceso
