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
 ARRAY = { 3,6,8,10,14,15,20,30,66,99 }
CASE-1:   key element = 6
                        Iteration-1:       low = 0 ; high = 9 ; mid = 4
                                                              a[4] = 14
                                                              Key < a[4]

                         Iteration-2:        low = 0 ; high = 4 ; mid = 2
                                                              a[2] = 8
                                                              Key < a[2]
 
                            Iteration-3:          low = 0 ; high = 2 ; mid = 1
                                                              a[1] = 6
                                                              Key < a[1]      
                                     Key element is found at position 1

CASE-2:     key element = 14        
                       Iteration-1:       low = 0 ; high = 9 ; mid = 1
                                                              a[4] = 14
                                                              Key = 14
                            Key element is found at position 1
                            
 CASE-3:       key element = 99
                         Iteration-1:        low = 0 ; high = 9 ; mid = 4
                                                              a[4] = 14
                                                              Key > a[4]
 
                           Iteration-2:          low = 9 ; high = 2 ; mid = 7
                                                              a[7] = 30
                                                              Key > a[7] 
                             
                            Iteration-3:          low = 8 ; high = 9 ; mid = 8
                                                              a[8] = 66
                                                              Key > a[8] 
     
                            Iteration-4:          low = 9 ; high = 9 ; mid = 9
                                                              a[9] = 99
                                                              Key > a[9]      

                            Key element is found at position 9                                
                              





        
    


