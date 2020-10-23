#include<stdio.h>
int main()
{
int n,i,min,j,temp;
printf("enter the size of array: ");
scanf("%d",&n);
int a[n];
printf("\n elements of array:\n");
for(i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
for (i=0;i<n-1;i++)
{
min = i;
for(j=i+1;j<n;j++)
{
if(a[j]<a[min])
{
min = j;
}
}

if(min!=i)
{
temp = a[i];
a[i] = a[min];
a[min] = temp;
}
}

printf("sorted array is : ");
for(i=0;i<n;i++)
{
printf("%d\t",a[i]);
}
return 0;
}
