---
title: Selection sort C++/JavaScript
---
Selection sort is another algorithm of sorting an array of elements, it is a lot faster than a usual Bubble sort(not sure that i did it well)
# C++
```
#include "stdafx.h"
#include <iostream>
using namespace std;
int i, j;
void SelectionSort(int A[], int n) //function for selection sort
{
int count, key;
for (i=0; i<n-1; i++)
{
count=A[i]; key=i;
for (j=i+1; j<n; j++)
if (A[j]<A[key]) key=j;
if (key!=i)
{
A[i]=A[key];
A[key]=count;
}
}
cout<<"Vectorul curent  ";
for (i=0; i<n; i++) cout<<A[i]<<" "; //afisarea vectorului
}
//главная функция
void main()
{
setlocale(LC_ALL, "Ro");
int n, A[1000];
cout<<"Numarul de elemente > "; cin>>n;
for (i=0; i<n; i++) //afisarea vectorului
{ cout<<i+1<<" elementul > "; cin>>A[i]; }
SelectionSort(A, n);
system("pause>>void");
}
```
