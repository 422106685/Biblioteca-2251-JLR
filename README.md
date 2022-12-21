# Biblioteca-2251-JLR
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <locale.h>
#include <conio.h>

 	///configuración al idioma español
void ConfiguraIdioma(){
	//Cambia al idioma Español   
	struct lconv *lcPtr;
	setlocale(LC_ALL, "spanish");
	lcPtr = localeconv();

	//Configura cantidades para México
	lcPtr->decimal_point = ".";
	lcPtr->thousands_sep = ",";
	lcPtr->grouping = "3";	
}

	//Imprime caratula
void caratula(){
	
	ConfiguraIdioma();
	printf("\nUniversidad Nacional Autónoma de México\n");
	printf("Facultad de Estudios Superiores Acatlán\n");
	printf("Licenciatura en Matemáticas Aplicadas y Computación\n");
	printf("Programación II\n");
	printf("Grupo 2251\n");
	
}
	//Queda en espera de recibir una tecla
void alto(){
	
	printf("\n Pulse tecla para continuar");
	getch();	
}

int generapseudoaleatorios(int n){
	
	return(rand()%n);
}
void fin(){
	printf("\nFin de ejecución.");
printf("\nPulse tecla para finalizar la ejecución");
	getch();
}
