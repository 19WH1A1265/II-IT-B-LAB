# Aim:
To write a program using non-recursive functions that perform the linearimg searching operations for a key value in a give list of integers

## Explanation:
The method of linear search must be stright forward.It loops through the array,starting from the beginning until it finds an element in the array.If the val argument was 20 the function would returns -1

### Step by Step procedure:
#include<stdio.h>
int Iterativelinear_search(int a[] , int n , int key )
{
    int i ;
    for (i =0 ;i < n ; i++)
        if (a[i] == key)
            return i ;
    return -1;
}
int main(void)
{
    int a[] = { 10,6,8,15,2,3,14,99,66,30 };
    int n = 9;
    int key =66;
    int index =Iterativelinear_search(a ,n , key);
    if (index != -1)
        printf("digit %d is present at index %d", key,index);
    else
        printf("digit %d is not present",key);
        return 0;
}
        
    

    
