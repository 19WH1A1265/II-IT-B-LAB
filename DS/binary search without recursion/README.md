# Aim:
To write a program to search an element in an array by using binary search without recursive method 

## Description:
In a non recurvise binary search if the val argument is not initially found in the array using the pointers,you can eliminate half of the possibilites by checking whether the middle array element is bigger or smaller than the given val argument.

### Step by Step procedure:
#include<stdio.h>
int Iterative_binarysearch(int arr[], int i, int n, int element)
{
    while(i <= n)
    {
        int mid = (i+n)/2;
        if(arr[mid]==element){
            return mid;
        }    
        else if(arr[mid]<element){
            i = mid + 1;
        }
        else{
            n = mid-1;
        }
    }
    return -1;
}
int main()
{
    int arr[] = {3,6,8,10,14,15,20,30,66,99};
    int n=10,element;
    printf("enter the element : ");
    scanf("%d",&element);
    int pos = Iterative_binarysearch(arr,0,n-1,element);
    if(pos == -1){
        printf("element not found");
    }
    else
    {printf("elment %d found at %d",element,pos);
    }
    return 0;
}
        
    


