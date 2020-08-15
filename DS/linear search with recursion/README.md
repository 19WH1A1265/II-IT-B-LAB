# Aim:
To write a program using recursive functions that perform the linear search operations for a key value in a given list of integers

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
    int key = 0;
    int index =Iterativelinear_search(a ,n , key);
    if (index != -1)
        printf("digit %d is present at index %d", key,index);
    else
        printf("digit %d is not present",key);
        return 0;
}
        
    

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
    int key = 0;
    int index =Iterativelinear_search(a ,n , key);
    if (index != -1)
        printf("digit %d is present at index %d", key,index);
    else
        printf("digit %d is not present",key);
        return 0;
}


ARRAY: { 10,6,8,15,20,3,14,99,66,30 }
CASE-1: key element = 66
      Iteration-1:       a[0] = 10
                                 Key ! = a[0]

       Iteration-2:        a[1] = 6
                                   Key ! = a[1]

       Iteration-3:        a[2] = 8
                                   Key ! = a[2]

      Iteration-4:           a[3] = 15
                                    Key ! = a[3]

      Iteration-5:              a[4] = 20
                                     Key ! = a[4]

       Iteration-6:             a[5] = 3 
                                     Key ! =a[5]

       Iteration-7:             a[6] = 14 
                                       Key ! = a[6]
        
    
       Iteration-8:              a[7] = 99
                                        Key ! = a[7]

        Iteration-9:              a[8] = 66
                                         Key ! = a[8]    
                                                                    {Case Passed}
     
                     We get output as:      66 found at position 8
    

      
    

    
    
