# Multiplication_array
#include<stdio.h>
void main()
{
int m,n,p,q;
printf("Enter a number of rows : ");
scanf("%d",&m);
printf("Enter a number of columns : ");
scanf("%d",&n);
int arr[m][n];
  
for(int i=0;i<m;i++)
{
    for(int j=0;j<n;j++)
        {   printf("Enter [%d][%d] element  : ",i,j);
            scanf("%d",&arr[i][j]);
        }
}
printf("\n\n"); 
printf("First matrix : ");
printf("\n");
for(int i=0;i<m;i++)
{
    for(int j=0;j<n;j++)
    { 
        printf("%d ",arr[i][j]);
    }
            printf("\n");
}

printf("\n");
printf("Enter a number of rows : ");
scanf("%d",&p);

printf("Enter a number of columns : ");
scanf("%d",&q);
int brr[p][q];
for(int i=0;i<p;i++)
{
    for(int j=0;j<q;j++)
    {   
        printf("Enter [%d][%d] element  : ",i,j);
        scanf("%d",&brr[i][j]);
    }
}
printf("\n\n");
printf("second matrix : ");
printf("\n");
for(int i=0;i<p;i++)
{
    for(int j=0;j<q;j++)
    { 
        printf("%d ",brr[i][j]);
    }
        printf("\n");
}

printf("\n");
if(n!=p)
printf("The matrices do not multiplied");
else
{
printf("The multiplication of given matrix \n");
int res[m][q];
for(int i=0;i<m;i++)
{
    for(int j=0;j<q;j++)
    {
        res[i][j]=0;
        for(int k=0;k<n;k++)
        {
            res[i][j]+=arr[i][k]*brr[k][j];
        }
    
        printf("%d  ",res[i][j]);
        }
        printf("\n");
}
}
}
