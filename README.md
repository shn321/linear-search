# linear-search
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[30],n,i,pos,key;
    int lsearch (int[],int,int);
    printf("\nEnter no of elements");
    scanf("%d",&n);
    printf("\nEnter %d value",n);
    for(i=0;i<n;i++)
        scanf("%d",&arr[i]);
    printf("Enter key value");
    scanf("%d",&key);
    pos=lsearch (arr,n,key);
    if(pos==-1)
        printf("\n search no %d is not found",key);
    else
        printf("\n search no %d is found at index %d",key,pos);
        getch();
}
int lsearch (int arr[],int n,int key)
{
    int pos=-1,i;
    for(i=0;i<n;i++)
    {
        if (arr[i]==key)
        {
            pos=i;
            break;
        }
    }
    return pos;
}
