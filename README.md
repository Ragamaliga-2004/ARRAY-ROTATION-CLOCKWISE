# ARRAY-ROTATION-CLOCKWISE
Given an array Arr[ ] of N integers and a positive integer K. The task is to cyclically rotate the array clockwise by K. Note : Keep the first of the array unaltered.

Input Format

Input: Enter Value of N Enter Array Elements Enter value k.

Sample Input: 5 ---Value of N {10, 20, 30, 40, 50} ---Element of Arr[] 2 Value of K 2 Value of K

Constraints

_

Output Format

Output:

Display Given Array elements in clockwise direction according to k Value.

Sample Output: 40 50 10 20 30

Sample Input 0

6
10 20 30 40 50 60
3
Sample Output 0

10 40 50 60 20 30
Explanation 0

IN Clock, range starts from 0 to 60.
So in the given array elements arr={10, 20, 30, 40, 50, 60}
value of k is arr[3]
so, arr[3] = 40
But first element should be the same.  
So order of array was {10, 40, 50, 60, 20, 30}
Sample Input 1

0
0
0

Sample Output 1

0
___________________________________________________________________________________________________________________________________________________________________________________________
#include<stdio.h>
int main() 
{
    int n,v,arr[20],j,i;
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    
    scanf("%d",&v);
    if(n>v){
        printf("%d ",arr[0]);
        for(j=n-v;j<n;j++)
        {
           printf("%d ",arr[j]);
        }
        for(i=1;i<n-v;i++){
            printf("%d ",arr[i]);
        }
    }
    else{
        printf("0");
    }
    return 0;
}
