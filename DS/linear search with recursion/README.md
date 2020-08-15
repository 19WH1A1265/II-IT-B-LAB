# Aim:
To write a program using recursive functions that perform the linear seach operations for a key value in a give list of integers

## Description:
The linear search recursion method is similar except it works backwards from the end of the array to start.Both linear search solutions return the same value and posses the same big O time complexity of O(n).

### Step by Step Procedure:#include<stdio.h>
int Recursivelinear_search(int a[] , int key , int index , int n)
{
    int i = 0;
    if(index >= n)
    {
        return 0;
    }
    else if (a[index] == key)
    {
        i = index + 1 ;
        return i ;
    }
    return Recursivelinear_search(a , key , index+1 , n);
}
int main()
{
    int i;
    int n = 9 ;
    int a[] = { 10,6,8,15,20,3,14,99,66,30 };
    int key = 0;
    i = Recursivelinear_search(a , key , 0 , n);
    if (i != 0)
    {
        printf("digit %d is present at %d " ,key,i);
    }    
    else
    {
        printf("digit %d is not present",key);
    }
    return 0;
}    
    
    

    
    
