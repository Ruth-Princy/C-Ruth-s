# C-Ruth-s
Here you can find some simple basic programs in C language
finding max no of subsets
#include<stdio.h>
void subset(int arr[],int n,int i,int soln[])
{
    if(i==n)
    {

        for(i=0;i<n;i++)
    {
        if(soln[i]==1)
        printf("%d ",arr[i]);
    }
    printf("\n");
    }
        else
        {
            soln[i]=1;
             subset(arr,n,i+1,soln);
             soln[i]=0;
            subset(arr,n,i+1,soln);

        }
}
int main()
{
    int n,i;
    scanf("%d",&n);
    int arr[n];
    int soln[n];
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }

    subset(arr,n,0,soln);
}
