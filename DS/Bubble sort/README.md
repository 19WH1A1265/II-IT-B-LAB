Bubble  sorting
Aim of the experiment:
To perform bubble sort of an unsorted and sorted array. 
Array (i):  5,6,7,8,9
Array (ii): -2,5,3,-6,9
Array (iii): 2,1,6,5,7
Brief description of Bubble sort:
Bubble Sort is a simple algorithm which is used to sort a given set of n elements provided in form of an array with n number of elements. Bubble Sort compares all the element one by one with the adjacent elements and sort them based on their values.
If the given array has to be sorted in ascending order, then bubble sort will start by comparing the first element of the array with the second element, if the first element is greater than the second element, it will swap both the elements, and then move on to compare the second and the third element, and so on.
If we have total n elements, then we need to repeat this process for n-1 times.
Step-by-step-procedure:
code:
#include <stdio.h>
int main()
{
  int array[100], n, i, j, k=1, swap;
  printf("Enter number of elements\n");
  scanf("%d", &n);
  printf("Enter %d integers\n", n);
  for (i = 0; i < n; i++)
    scanf("%d", &array[i]);
  for (i = 0; i < n; i++)
  {
    if(array[i] > array[i+1])
    {
        k = 0;
        break;
    }
  }
  if(k==1)
  {
    printf("The elements are already sorted\n");
  }
  else{
  for (i = 0 ; i < n - 1; i++)
  {
    for (j = 0 ; j < n - i - 1; j++)
    {
      if (array[j] > array[j+1]) 
      {
        swap  = array[j];
        array[j]   = array[j+1];
        array[j+1] = swap;
      }    
    }
  }
  printf("Sorted list in ascending order:\n");
  for (i = 0; i < n; i++)
     printf("%d\n", array[i]);
  }
  return 0;
}


1.	Starting with the first element, compare the current element with the next element of the array. 
2.	If the current element is greater than the next element of the array, swap them. 
3.	If the current element is less than the next element, move to the next element. 
4.	Repeat step 1.
Output obtained: 

(i)Bubble sorting of sorted array
Procedure of obtaining output:
1.	Read elements of the array and number of the array elements.
2.	Here n = 5 and array = {5 , 6, 7,8,9}
3.	In bubble sorting, the elements of the array are swapped and arranged in ascending order.
4.	But, in this case, the elements are already sorted.
5.	So, after entering the elements (that are already sorted), it
6.	prints"The elements are already sorted."

 ii) Bubble sorting of sorted array
Procedure of obtaining output:
1.	Read elements of the array and number of the array elements.
2.	Here n = 5 and array = {-2,5,3,-6,9}
3.	As the number of elements is 5, the number of iterations will be 4(n-1).
1st iteration
-2, 5, 3, -6, 9
   5>3, so it swaps
-2, 3, 5, -6, 9
5 > -6 so it swaps
-2 ,3, -6 ,5, 9
2nd iteration
2 , 3, -6,5, 9
3>-6 so it swaps
-2 , -6, 3 , 5, 9
3rd iteration
-2 , -6 , 3 , 5 , 9
-2>-6 so it swaps
-6 , -2 , 3 , 5, 9
 4th iteration 
-6 , -2 , 3 , 5 , 9
By the end of the fourth iteration, the fourth greatest element lies at the end. Here, it is 4 which is last fourth from the end. And the array elements (after the com
pletion of 4th iteration) are:
       -6	      -2	       3	       5	       9
       
       (iii)Bubble sorting of unsorted array
Procedure of obtaining output:
1.	Read elements of the array and number of the array elements.
2.	Here n = 5 and array = {2,1,6,5,7}
3.	As the numbers of elements present are 5, the number of iterations will be 4(n-1).

1st iteration:
2, 1, 6, 5, 7
2>1 so it swaps
1 , 2 , 6 , 5 , 7

2nd iteration
1, 2 , 6 , 5 , 7
1<2 so iis remain same
      1,2, 6, 5, 7
3rd iteration
1 , 2 , 6 , 5 , 7
6>5 so it swaps
1, 2 ,5, 6, 7
4th iteration
 1 , 2 , 5 , 6, 7
By the end of the fourth iteration, the fourth greatest element lies at the end. Here, it is 4 which is last fourth from the end. And the array elements (after the com
pletion of 4th iteration) are:
       1	        2	        5	        6	        7



