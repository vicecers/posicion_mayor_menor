```c++
#include <iostream>
using namespace std;

//constante para filas columnas
#define FILA 4  
#define COLUMNA 4

int main(int argc, char** argv) {

int matriz[FILA][COLUMNA] = {
            {44,  40, 79, 40},
            {68, 15, 120, 22},
            {56,  8,  33, 27},
            {6,  40,  13, 7}            
    };
  int menor = matriz[0][0];
  int mayor = matriz[0][0];
  int posf, posc;
  
   // Recorrer la matriz y comparar
    for (int y = 0; y < FILA; y++) {
        for (int x = 0; x < COLUMNA; x++) {
            if (matriz[y][x] > mayor){
            	mayor = matriz[y][x];
            	posf=y;
            	posc=x;
             } 
            if (matriz[y][x] < menor) {
            	menor = matriz[y][x];
            }
        }
    }
    
    cout << "Mayor: " << mayor << endl << "Posicion fila: " << posf << " Posicion columna: " << posc << endl;
    cout << "Menor: " << menor << endl;	
	return 0;
}
```
