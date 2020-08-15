# Aim:
To write a program to search an element in array by using binary search recursive method

## Description:
Binary search is used to find the position of an element in a sorted array.The array should be sorted prior to applying a binary search.

### Step by Step procedure:
#include <stdio.h>
int Recursivebinary_search(int a[] , int low , int high , int key)
{
    if(low > high)
    {
        return -1;
    }
    int mid = ( low + high) / 2;
    if ( a[mid] == key)
    {
        return mid;
    }
    else if(key < a[mid])
    {
        Recursivebinary_search(a , low , mid-1 , key);
    }
    else
        Recursivebinary_search(a , mid+1 , high , key);
}
int main()
{
    int a[] = { 3,6,8,10,14,15,20,30,66,99 };
    int digit;
    printf("enter the digit\n");
    scanf("%d",&digit);
    printf("digit is at %d\n",Recursivebinary_search(a, 0 , 9 , digit));
    return 0;
}    


    
    
