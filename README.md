#include<stdio.h>
void selectionsort (int[], int);
void main ()
{
  int a[10], n, i;
  scanf ("%d", &n);
  for (i = 0; i < n; i++)
    {
      scanf ("%d", &a[i]);
    }
  selectionsort (a, n);
}

void selectionsort (int a[], int n)
{
  int mpos, i, j, t;
  for (i = 0; i < n-1; i++)
    {
      mpos = i;
      for (j = i + 1; j < n; j++)
	{
	  if (a[mpos] > a[j])
	    {
	      mpos = j;
	    }
	}
	  t = a[mpos];
	  a[mpos] = a[i];
	  a[i] = t;
	}
    }
  for (i = 0; i < n; i++)
    printf ("%d\t", a[i]);
}
