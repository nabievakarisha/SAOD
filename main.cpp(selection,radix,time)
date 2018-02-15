#include <iostream>
#include <time.h>
#include <locale>

using namespace std;
void Zapolnenie(int *a, int *b ,int n){
    for (int i = 0; i < n; i++){
        a[i]=rand() % 11;
        b[i]= a[i];


}}
void Print(int *a, int n){
    for (int i = n-100; i < n; i++){
             cout << a[i] <<" ";

        }
}


void selection(int *ar, int size)
 {
    time_t start, end;
    time(&start);
     int i, j, mx, nmx;

     for(i = 0; i < size-1; i++)
       {
         mx=ar[i];
         nmx=i;
         for(j = i+1; j < size; j++)
           {
             if (ar[j]<mx)
                {
                 mx=ar[j];
                 nmx=j;
                 }
           }
          ar[nmx]=ar[i];
          ar[i]=mx;
           }

     time(&end);

           double seconds = difftime(end, start);
           printf("The time: %f seconds\n", seconds);
}
void radix(int *ar, int *br, int *cr, int sizeC, int sizeAB)
{
     clock_t start = clock();
    int i,k,n;
    k = sizeC;
    n = sizeAB;
    for (i = 0; i <= k; i++)
        cr[i]=0;
    for (i = 0; i < n; i++)
        cr[ar[i]]+=1;
    for (i = 1; i < k+1; i++)
        cr[i]+=cr[i-1];
    for (i = n-1; i >= 0; i--)
      {
         br[cr[ar[i]]-1]=ar[i];
         cr[ar[i]]-=1;
      }
clock_t end = clock();
double seconds = (double)(end - start) / CLOCKS_PER_SEC;
      printf("The time: %f seconds\n", seconds);

    }





int main()
{
    setlocale(LC_ALL, "Russian");
    int *a, *b, *c, *d, n, k = 11;
    cout << "Vvedite razmer\n";
    cin >> n;
    a= new int[n];
    b= new int[n];
    c= new int[n];
    d= new int[k];
    Zapolnenie(a,b,n);
    Print(a,n);
    selection(a,n);
    cout <<"\nOtsortirov. massiv(selection) \n" ;
    Print(a,n);
    cout <<"\nmassiv b:\n";
    Print(b,n);
    radix(b,c,d,k,n);
    cout <<"\nOtsortirov. massiv(radix)\n";
    Print(c,n);
    return 0;
}
