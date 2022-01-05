# oj-page-7
#1608
再见防御罩
#include<stdio.h>
void main()
{
    int n,m,z,h,v,b,c,d,e,i,j,k,count=0;
    int a[100][100]={0},zx[10],zy[10],zx1[10],zy1[10];
    scanf("%d%d%d%d%d",&n,&m,&z,&h,&v);
    for(i=0;i<z;i++)
    scanf("%d%d%d%d",&zx[i],&zy[i],&zx1[i],&zy1[i]);
    for(k=0;k<h;k++)
    {
        scanf("%d%d",&b,&c);
        for(i=b-1;i<c;i++)
        for(j=0;j<m;j++)
        a[i][j]=1;
    }
    for(k=0;k<v;k++)
    {
        scanf("%d%d",&b,&c);
        for(j=b-1;j<c;j++)
        for(i=0;i<n;i++)
        a[i][j]=1;
    }
    for(i=0;i<z;i++)
    {
        for(b=zx[i]-1;b<zx1[i];b++)
        for(c=zy[i]-1;c<zy1[i];c++)
        a[b][c]=0;
    }
    for(i=0;i<n;i++)
    for(j=0;j<m;j++)
    if(a[i][j]==1)
    count++;
    printf("%d",count);
}
