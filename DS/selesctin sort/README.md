#include <stdio.h>
void selection_sort(int* a);
int main()
{
    int i;
    int a[7];
    printf("pass 7 integers:\n");
    for(i=0; i<7;i++)
    scanf("%d",&a[i]);
    selection_sort(a);
    printf("Integers in sorted order:\n");
    for(i=0;i<7;i++)
    printf("%d  ", a[i]);
    return 0;
}
void selection_sort(int* a)
{
    int i, j, temp;
    for(i=1;i<=7;i++)
    {
       for(j=i+1; j<6; j++){
           if(a[i] > a[j]){
               temp = a[i];
               a[i] = a[j];
               a[j] = temp;
           }
       } 
    }
    return;
}
