//Sortare descrescatoare

#include<iostream>
#include<fstream>
using namespace std;
int n;
int V[100];

int main ()
{
    fstream f;
    f.open("input.dat",ios::in);
    f>>n;
    for(int i=1;i<=n;i=i+1)
    {f>>V[i];}
    int gata=0;
    int copie=n;
    while (gata==0)
    {
        gata=1;
        for(int i=1;i<n; i++)
        if (V[i]>V[i+1]) {
            swap (V[i], V[i+1]);
            gata=0;}
            n--;
    }
    n=copie;
    for(int i=1; i<=n; i++)
        cout<<V[i]<<" ";
}
