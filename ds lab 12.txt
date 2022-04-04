#include <stdio.h>
#include<stdlib.h>
#define MAX 10
int a[MAX]
int create(int);
void linear(int[],int);
void display(int[]);

int create(int num)
{
  int key;
  key=num%10;
  return key;
}
void linear(int a[MAX],int num )
{
  int i,count,flag,key;
  char ans='y';
  while(ans=='y')
  {
    flag=0;
    count=0;
    printf("enter 4 digit no\n");
    scanf("4%d",&key);
    key=create(num);
    if(a[i]==-1)
    {
      a[key]=num;
    }
    else
    {
      printf("collision detected\n");
      i=0;
      while(i<MAX)
      {
        if(a[i]==-1)
        count++;
        i++;
      }
      printf("collision avoided by linear probing\n");
      if(count==MAX)
      {
        printf("hash table full\n");
        dislay(a);
      }
      for(i=key+1;i<MAX;i++)
      {
        if(a[i]==-1)
        {
          a[i]=num;
          flag=1;
          break;
        }
      }
    }
    printf("do you wish to continue (y/n");
    fflush(stdin);
    scanf("%c",&ans);
  }
}
void display(int a[MAX])
{
  int i;
  printf("contents are\n");
  for (i=0;i<MAX;i++)
  printf("%d",a[i]);
}
void main()
{
    int ch;
    printf("1-linear prob\n");
    printf("2-create \n");
    printf("3-display\n" );
    printf
}