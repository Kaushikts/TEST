# TEST
#include<stdio.h>
#include<math.h>
int list[2];
void bleh(float price[],int N,int M)
{
  float diff[N][N],list[M],min,mini,minj,tmi,tmj;
  int item=0,tmpi,tmpj;
  for(int i=0;i<N;i++)
  {
    for(int j=0;j<N;j++)
      diff[i][j] = abs(price[i]-price[j])
  }
  min=diff[0][0];

  for(int i=0;i<N;i++)
  {
    for(int j=0;j<N;j++)
    {
      if(min>diff[i][j]&&diff[i][j]!=0)
      {
        min=diff[i][j];
        tmpi=i;tmpj=j;
      }
    }
  }

  list[0]=price[tmpi];
  list[1]=price[tmpj];
  for(int k=2;k<M;k++)
  {
    mini=diff[tmpi][0];minj[0][tmpj];
    for(int i=0;i<N;i++)
    {
      if(mini>diff[tmpi][i]&&diff[tmpi][i]!=0&&i!=tmpj)
      {
        mini=diff[tmpi][i];
        tmi=tmpi;tmj=i;
      }
      if(minj>diff[i][tmpj]&&diff[i][tmpj]!=0&&i!=tmpj)
      {
        minj=diff[i][tmpj];
        ti=i;tj=tmpj;
      }
    }
    if(mini<minj)
    {
      list[2]=price[tmj];
      tmpi=tmj;
    }
    else if(mini>=minj)
    {
      list[2]=price[ti];
      tmpj=ti;
    }
  }


}
void main()
{
float M,N,p[12];
printf("enter no of employees");
scanf("%f",&M);
printf("enter goodies");
scanf("%f",&N);
printf("enter cost");
for(i=0;i<N;i++)
scanf("%f"),&p[i]);
bleh(p,N,M);
for(i=0;i<M;i++)
print("%f",list[i])
}
