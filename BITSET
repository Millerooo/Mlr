
#include <iostream>
#include <fstream>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

using namespace std;

int main(int argc, char** argv)
{
	 int liczbaRekordow=0;
 ifstream file; //plik wejsciowy
 ifstream file2; //plik wejsciowy
 ifstream file3; //plik wejsciowy
 ofstream fileOut; //plik wynikowy do zapisu
 char* endptr; // to jest wskaźnik na miejsce, gdzie przy konwersji z systemu czworkowego wystąpi błąd - nieużywana zmienna
 long liczba, max, max2, max3; //liczba dziesietna, minimum z pliku
 string liczba1, liczba2 ,liczba3, liczba4, liczba5, liczba6,liczbaII,liczbaIII, rekord, rekord2, rekord3;  //dwie liczby w systemie czworkowym wczytujemy jako "string" bo mogą być dłuższe od long long
 file.open("dane_systemy2.txt");
 file2.open("dane_systemy2.txt");
 file3.open("dane_systemy2.txt"); //otworz plik liczb
 fileOut.open("wyjscie.txt"); //otworz plik do wynikow
 bool pierwszy = true;  //do algorytmu MINIMUM - zakładamy, że pierwsza liczba jest najmniejsza z dotychczas przeczytanych
 
 if(file.good())  //sprawdzenie czy plik istnieje
     while(!file.eof())        //petla wykonuje sie az program dojedzie do konca pliku
     {
               file>>liczba1 >> liczba2;
			   file2>>liczba3 >> liczba4;
			   file3>>liczba5 >> liczba6;   // wczyta dwie liczby z pliku (w wierszu) do 2 stringów
               liczba =  strtol(liczba2.c_str(), &endptr, 4);
               liczbaII =  strtol(liczba4.c_str(), &endptr, 4);
               liczbaIII =  strtol(liczba6.c_str(), &endptr, 4);
               //^konwersja z systemu czworkowego do dziesietnego, string (C++) trzeba zamienić na char * (C) funkcja .c_str()
               //zmienna endptr wskazuje na znak w stringu, który nie pasuje do systemu czwórkowego - tu niesprawdzone, bo zakładamy, że dane są poprawne!
               if(pierwszy) //jeśli to pierwsza liczba z pliku - będzie nowym MINIMUM
               {
                            max = liczba;
                            max2 = liczbaII;
                            max3 = liczbaIII;
                            pierwszy = false;
               }
               else{
               		bool rekord = false;
	               	if (liczba > max){
	               	max = liczba;
	               	rekord = true;
	               }
	               bool rekord2 = false;
	               if (liczbaII > max2){
	               	max2 = liczbaII;
	               	rekord2 = true;
	               }
	               bool rekord3 = false;
	               if (liczbaIII > max3){
	               	rekord3 = true;
	               	max3 = liczbaIII;
	               }
					   
					   

			    //jeśli to kolejna liczba z pliku...
                  if(liczba > max){
                  	liczbaRekordow ++;
				  } //... i jest mniejsza od dotychczasowego minimum...
                       max = liczba; // ... to nadpisz min
                       
                      if (rekord1 || rekord2 || rekord3 ) liczbaRekordow++;
					   
     }//eof() koniec pliku
 fileOut<< "58.3: " << max <<endl; //zapisanie najmniejszej liczby z pliku czworkowego do pliku wynikowego
 file.close();
 file2.close();
 file3.close();
 fileOut.close();
 return 0;
}
}
