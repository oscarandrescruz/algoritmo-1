# algoritmo-1
#include "stdafx.h"
#include "math.h"
#include "conio.h"
#include <iostream>

using namespace std;

float serie(float x,float n);
float factorial(float s);

int main() 
{float numero,exponente,total;
 cout<<"ingrese un numero";
 cin>>numero;
 cout<<"ingrese el exponente";
 cin>>exponente;
 total=serie(numero,exponente);
 cout<<"la suma de la series es:"<<total;
 system("pause");
 return 0;	
}
float serie(float x,float n)
{float suma=0,i,sig=1;
 for(i=1;i<=n;i++)
 {suma=suma+(sig*(pow(x,i)/factorial(i)));
  sig=sig*(-1);
 }
 return suma;
}
float factorial(float s)
{float j,fac=1;
 for(j=1;j<=s;j++)
 { fac=fac*j;
 }
 return fac;
}

