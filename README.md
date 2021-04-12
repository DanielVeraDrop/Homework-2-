# Homework-2-
#include <iostream>
#include <string>
#include <stdio.h>
using namespace std;
//Justin Daniel Vera Paco
//UCSP (Ciencias de la Computación_CComp2-1)
//Segundo trabajo
//---3 en raya (1era parte)---
//demore bastantes horas haciendolo y olvide que era con explicacion ;-; intentare hacerlo lo mejor posible XD
int escoger() //ayuda al usuario a escoger entre x y o
{
  char opcion;

  while(true) {
    cout<<"escoja entre 'X' ó 'O' :"; //escribe en pantalla una sugerencia de que escoger
    cin>>opcion;
    if( opcion != 'X' && opcion !='O' && opcion != 'x' && opcion !='o')//repite en bucle la funcion cuando escribes un valor erroneo hasta que lo escribas correctamente
      cout << "Debe escoger X u O" <<endl;
    else{
      cout << "Usted escogio ser "<< opcion << "\n";//y esto en caso de hacerlo correctamente 
  if(opcion == 'X' || opcion == 'x')
    return 1;//estos return los hice ya que no encontre otra forma de identificar el 'X' y el 'O' fuera del main
  else
  return 2; 
    }
  }
}
void ubicacionX(){
  char matriz[3][3]={'1','2','3','4','5','6','7','8','9'};  //Declaración de la matriz
  char numero;
  cout <<""<<matriz[0][0]<<" | "<<matriz[0][1]<<" "<<" | "<<matriz[0][2]<<" "<<"\n"; //imprimo toda la matriz, de forma individual ya que al ser impar '|' con par '---' se me complico hacerlo con for
  cout <<"-----------"<<"\n";
  cout <<""<<matriz[1][0]<<" | "<<matriz[1][1]<<" "<<" | "<<matriz[1][2]<<" "<<"\n";
  cout <<"-----------"<<"\n";
  cout <<""<<matriz[2][0]<<" | "<<matriz[2][1]<<" "<<" | "<<matriz[2][2]<<" "<<"\n";
  
  cout <<"donde quieres colocar la variable?(del 1 al 9):"; //sugerencia para colocar el numero y realizar el cambio
  cin >> numero;  //cita la ubicacion del X
    if(numero == '1')//combinacion de if y else if para que cada numero sea una ubicación distinta
      matriz[0][0] = 'X';
    else if(numero == '2')
      matriz[0][1] = 'X';
    else if(numero == '3')
      matriz[0][2] = 'X';
    else if(numero == '4')
      matriz[1][0] = 'X';
    else if(numero == '5')
      matriz[1][1] = 'X';
    else if(numero == '6')
      matriz[1][2] = 'X';
    else if(numero == '7')
      matriz[2][0] = 'X';
    else if(numero == '8')
      matriz[2][1] = 'X';
    else if(numero == '9')
      matriz[2][2] = 'X';
    else {
      cout<<"Movimiento no identificado...";
    } //se imprime nuevamente el 3 en raya pero esta vez con el factor cambiado
    cout <<""<<matriz[0][0]<<" | "<<matriz[0][1]<<" "<<" | "<<matriz[0][2]<<" "<<"\n";  
    cout <<"-----------"<<"\n";
    cout <<""<<matriz[1][0]<<" | "<<matriz[1][1]<<" "<<" | "<<matriz[1][2]<<" "<<"\n";
    cout <<"-----------"<<"\n";
    cout <<""<<matriz[2][0]<<" | "<<matriz[2][1]<<" "<<" | "<<matriz[2][2]<<" "<<"\n";
} 

void ubicacionY() //repetido el anterior pero cambiando el factor "X" por "O"
{
  char matriz[3][3]={'1','2','3','4','5','6','7','8','9'};  
  char numero;
  cout <<""<<matriz[0][0]<<" | "<<matriz[0][1]<<" "<<" | "<<matriz[0][2]<<" "<<"\n"; 
  cout <<"-----------"<<"\n";
  cout <<""<<matriz[1][0]<<" | "<<matriz[1][1]<<" "<<" | "<<matriz[1][2]<<" "<<"\n";
  cout <<"-----------"<<"\n";
  cout <<""<<matriz[2][0]<<" | "<<matriz[2][1]<<" "<<" | "<<matriz[2][2]<<" "<<"\n";

  cout <<"donde quieres colocar la variable?(del 1 al 9):";
  cin >> numero;  
    if(numero == '1')
      matriz[0][0] = 'O';
    else if(numero == '2')
      matriz[0][1] = 'O';
    else if(numero == '3')
      matriz[0][2] = 'O';
    else if(numero == '4')
      matriz[1][0] = 'O';
    else if(numero == '5')
      matriz[1][1] = 'O';
    else if(numero == '6')
      matriz[1][2] = 'O';
    else if(numero == '7')
      matriz[2][0] = 'O';
    else if(numero == '8')
      matriz[2][1] = 'O';
    else if(numero == '9')
      matriz[2][2] = 'O';
    else {
      cout<<"Movimiento no identificado...";
    }
    cout <<""<<matriz[0][0]<<" | "<<matriz[0][1]<<" "<<" | "<<matriz[0][2]<<" "<<"\n";  
    cout <<"-----------"<<"\n";
    cout <<""<<matriz[1][0]<<" | "<<matriz[1][1]<<" "<<" | "<<matriz[1][2]<<" "<<"\n";
    cout <<"-----------"<<"\n";
    cout <<""<<matriz[2][0]<<" | "<<matriz[2][1]<<" "<<" | "<<matriz[2][2]<<" "<<"\n";
} 

int main() {  
  if(escoger()==1)//aplicamos la funcion escoger y si esta es = 1 (por el return hecho anteriormente)se aplicara el cambio con 'X'
    ubicacionX();
  else{ // de lo contrario se aplicara el valor con 'O'
    ubicacionY();
  }
}
