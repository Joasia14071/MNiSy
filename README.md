# MNiSy
library
#include <iostream>
#include <fstream>
#include <iomanip>
#include <cstdlib>

using namespace std;

// losuje liczbe pseudolosowa [0, max]

int losowanie (int max)
{
    return rand () % max;
}

string bufor;

int main()
{
    cout << "Losujemy ile ksiazek klient wypozyczy!" << endl;
    cout << "Wypozyczy "<<losowanie(100)<< " ksiazke/ksiazek" <<endl;
    // wczytywanie

    ifstream baza("baza.txt");
    if (!baza)
    {
        cout << "Nie mozna otworzyc pliku";
        getchar();
        return 1;
    }
    while (getline(baza,bufor))
        cout << bufor<<endl;
    getchar();
    return 0;
}

