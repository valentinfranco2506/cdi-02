Alumno: Valentin Franco
Curso:  4 1 avionica
Materia: Control de Interfaces

Colaboradores: Thiago Albornoz,Sebastian Erbino

#include <stdio.h>
int main (void) {

    int monto;
    int por_retirar;
    int retirado=0;
    int billete_de_1=0;
    int billete_de_5=0;
    int billete_de_10=0;
    int billete_de_20=0;
    int billete_de_50=0;
    int billete_de_100=0;

    printf("Ingrese un monto a retirar: ");
    scanf("%d", &monto);

    if (monto>5000) {
    printf ("Inválido");
        return 2;
    }
    else if (monto<20) {
    printf ("Inválido");
        return 1;
    }
 
    por_retirar = monto - retirado;
    for (billete_de_100=0; por_retirar>=100; billete_de_100++) {
        retirado += 100;
        por_retirar = monto - retirado;
    }
    for (billete_de_50=0; por_retirar>=50; billete_de_50++) { 
        retirado += 50;
        por_retirar = monto - retirado;
    }
    for (billete_de_20=0; por_retirar>=20; billete_de_20++) {
        retirado += 20;
        por_retirar = monto - retirado;
    }
    for (billete_de_10=0; por_retirar>=10; billete_de_10++) {
        retirado += 10;
        por_retirar = monto - retirado;
    }
    for (billete_de_5=0; por_retirar>=5; billete_de_5++) {
        retirado += 5;
        por_retirar = monto - retirado;
    }
    for (billete_de_1=0; por_retirar>=1; billete_de_1++) { 
        retirado += 1;
        por_retirar = monto - retirado;

    }

    printf ("Billetes de 1= %d\n", billete_de_1);
    printf ("Billetes de 5= %d\n", billete_de_5);
    printf ("Billetes de 10= %d\n", billete_de_10);
    printf ("Billetes de 20= %d\n", billete_de_20);
    printf ("Billetes de 50= %d\n", billete_de_50);
    printf ("Billetes de 100= %d\n", billete_de_100);
} 
