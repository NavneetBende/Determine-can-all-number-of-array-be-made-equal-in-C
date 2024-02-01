Can all number of an array be made equal
Here, in this page we will discuss can all the number of an array be made equal in C.

Let take an array arr[]. We need to check if all the numbers of an array can be  made equal to a particular number. In a single operation, any element of the array can be either multiplied by 2 or by 3. If it’s  possible to make all the array elements equal with the given operation then print Yes else print No

can all number of array be made equal
While loop in C
Keypoint
In this section we will learn about basic knowledge which we need to know before coding the above Program. So we must have knowledge of what is an array? 

What is an array?
An array is a data structure, it is collection of similar data elements which is stored at contiguous memory locations in which each data element can be accessed directly by only using its index number.
Algorithm :
Start traversing the array and check if the number is divisible by 2.
If it is divisible, divide the array element by 2.
Similarly, check if the array element is divisible by 3.
If it is divisible, divide the array element by 3.
Then, check the remaining elements with the first element of the array.
If they are equal, the array can be made equal.
Related Pages
Finding Arrays are disjoint or not

Determine Array is a subset of another array or not

Finding Minimum sum of absolute difference of given array

Sort an array according to the order defined by another array 

Replace each element of the array by its rank in the array

Code in C
//Write a program to check can all number of an array be made equal

#include <stdio.h>

int EqualNumbers(int a[], int n)
{
    for (int i = 0; i < n; i++) {

       // Divide number by 2
       while (a[i] % 2 == 0)
           a[i] /= 2;

       // Divide number by 3
       while (a[i] % 3 == 0)
            a[i] /= 3;

       if (a[i] != a[0]) {
           return 0;
       }
    }

    return 1;
}

// Driver code
int main()
{
    int a[] = { 50, 75, 100 };

    int n = sizeof(a) / sizeof(a[0]);

    if (EqualNumbers(a, n))
       printf("Yes");
    else
       printf("No");

    return 0;
}
Output :
Yes
