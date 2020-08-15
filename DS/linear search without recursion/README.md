# Aim:
To write a program using non-recursive functions that perform the linearimg searching operations for a key value in a give list of integers

## Explanation:
The method of linear search must be stright forward.It loops through the array,starting from the beginning until it finds an element in the array.If the val argument was 20 the function would returns -1

### Step by Step procedure:
 #include<stdio.h>
int Iterativelinear_search(int a[] , int n , int key)
{
    int i ;
    for (i =0 ;i < n ; i++)
        if (a[i] == key)
            return i ;
    return -1;
}
int main(void)
{
    int a[] = { 10,6,8,15,20,3,14,99,66,30 };
    int n = 9;
    int key = 66;
    int index = Iterativelinear_search(a , n , key);
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
                                                                                         { case passed }  
                           
                    CASE-2: key element = 66
                           
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
                          
                          Iteration-10:         a[9] = 30
                                                         Key ! = a[9]
                      
                      { Here the key element is not equals to any of the elements in the given array}

We get output as:     element not found.

                      
                                                                        
                                                           




        
    

    
