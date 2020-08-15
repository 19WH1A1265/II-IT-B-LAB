# Aim:
To write a program to search an element in array by using binary search recursive method

## Description:
Binary search is used to find the position of an element in a sorted array.The array should be sorted prior to applying a binary search.

### Step by Step procedure:
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
                              




