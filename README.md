# Cocktail-Sort-1
#include <iostream> using namespace std;
void Cocktail_Sort(int Array[], int n)
{
bool swapped = true; int start = 0;
int end = n - 1;


while (swapped)
{
swapped = false;
for (int i = start; i < end; ++i)
{
if (Array[i] > Array[i + 1])
{
swap(Array[i], Array[i + 1]); swapped = true;
}
}
if (!swapped)
break;

swapped = false;
--end;


for (int i = end - 1; i >= start; --i)
{
if (Array[i] > Array[i + 1])
{
swap(Array[i], Array[i + 1]); swapped = true;
}
}
++start;
}
}


void Print_Array(int Array[], int n)
{
for (int i = 0; i < n; ++i) cout << Array[i] << " "; cout << endl;
}


int main()
 
{
int Array[] = { 5, 1, 4, 2, 8, 0, 2 };
int n = sizeof(Array) / sizeof(Array[0]); Cocktail_Sort(Array, n);
cout << "Sorted Array:"; Print_Array(Array, n); return 0;
}

 
